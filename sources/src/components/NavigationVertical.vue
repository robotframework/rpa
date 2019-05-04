<template>
<section>
<b-nav  tag="nav" toggleable="md" vertical id="navigation" class="col-sm-3 col-md-2 d-none d-md-block sidebar">
  <b-navbar-brand >
        <b-img style="margin:0;padding:15%;" :src="require('@/assets/img/ROBOTFW_Mark_White_LOW_cropped.png')" class="img-fluid" alt="Robot Frameworkg logo"/>
        
  </b-navbar-brand>
  <p style="text-transform: none;font-size: 0.5em;color:#999;text-align:left;padding:10%;">The Robot Framework Foundation maintains RPA functionality as part of ongoing Robot Framework development. <br><br>The initial development of Robot Framework's RPA functionality was sponsored by five Foundation member companies.</p>
    <b-nav-item :href="item.href" v-for="(item,index) in pages" :key="index">{{item.title}}</b-nav-item>
</b-nav>

</section>
</template>

<script>
export default {
  // props: ["pages"],
  data() {
    return {
      pages: [
        {
          title: "Siili Solutions",
          href: "https://www.siili.com"
        },
        {
          title: "Knowit",
          href: "https://www.knowit.fi"
        },
        {
          title: "VALA Group",
          href: "https://www.valagroup.com"
        },
        {
          title: "Qentinel",
          href: "https://qentinel.com"
        },
        {
          title: "Eficode",
          href: "https://www.eficode.com"
        }
      ]
    };
  }
};
</script>
