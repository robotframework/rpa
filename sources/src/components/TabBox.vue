<template>
  <div class="row">
        <b-tabs v-model="tabIndex" pills class="card nav-fill col-lg-12 m-3">
          <b-tab v-for="(tab,index) in data" :key="index" :title="tab.title" class="p-1" @click="changeTab">
            <div id="{tab.title}-standard" class="card-body row">
              <div v-for="(item,index) in tab.items" :key="index" class="link  col-md-4">
                <b-embed v-if="typeof item.src != 'undefined'" type="iframe"
                        :src="item.src"
                        allowfullscreen
                ></b-embed>
                <a :href="item.href" target="_blank">{{item.title}}</a>
                <p v-html="item.text"/>
              </div>
            </div>
          </b-tab>
        </b-tabs>
  </div>
</template>

<script>
export default {
  props: ["data"],
  data() {
    return {
      section: document.getElementById(this.$route.hash.replace("#", "")),
      tabIndex: this.tabIndexValue()
    };
  },
  methods: {
    changeTab: function() {
      this.$router.push({
        path: this.$route.hash,
        query: { tab: this.tabIndex }
      });
    },
    tabIndexValue: function() {
      console.log(document.getElementById(this.$route.hash.replace("#", "")));
      return typeof this.section != "undefined" ? this.$route.query.tab : 0;
    }
  }
};
</script>
