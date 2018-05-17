<template>
<section>
<b-nav  tag="nav" toggleable="md" vertical id="navigation" class="col-sm-3 col-md-2 d-none d-md-block sidebar">
  <b-navbar-brand >
        <b-img style="margin:0;padding:15%;" :src="require('@/assets/img/ROBOTFW_Mark_White_LOW_cropped.png')" class="img-fluid" alt="Robot Frameworkg logo"/>
        
  </b-navbar-brand>
  <p style="text-transform: none;font-size: 0.5em;color:#999;text-align:center;padding:5%;">The initial development of Robot Framework RPA has been sponsored by five Finnish companies who are also members of the Robot Framework Foundation.</p>
    <p v-for="(item,index) in pages" :key="index">{{item}}</p>
</b-nav>

</section>
</template>

<script>
export default {
  // props: ["pages"],
  data() {
    return {
      pages: ["Siili Solutions", "Knowit", "VALA Group", "Qentinel", "Eficode"]
    };
  }
};
</script>
