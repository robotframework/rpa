<template>
  <div class="row justify-content-between no-gutters">
    <div v-if="data.text != ''" class="col-md-5 col-lg-4 order-1 textblock-left p-3">
      <h1 v-html="data.header"/>
    </div>
    <div v-else class="col-lg-12 order-1 pl-3 pt-3 pd-0 md-0 textblock-left">
      <h1 class="m-0 p-0" v-html="data.header"/>
    </div>
    <div v-if="data.text != ''" class="col order-2 textblock-right ml-1 p-3">
      <div v-html="data.text"/>
    </div>
     <div v-if="data.twitter == true" class="col-md-12 col-lg-3 order-3 textblock-right ml-1 p-3">
       <twitter-timeline class="p-xs-5 p-lg-0" id="robotframework" widget-class="twitterprofile" sourceType="profile" :options="options"/>
     </div>
  </div>
</template>

<script>
import Timeline from "vue-tweet-embed/timeline";
export default {
  props: ["data"],
  components: {
    "twitter-timeline": Timeline
  },
  data() {
    return {
      options: {
        theme: "light",
        tweetLimit: "3",
        chrome: ["nofooter", "noscrollbar"]
      }
    };
  }
};
</script>
