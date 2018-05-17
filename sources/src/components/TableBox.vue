<template>
  <div class="row ">
       <div class="table-responsive">
         <b-table :items="data.rows"></b-table>
       </div>
  </div>
</template>

<script>
export default {
  props: ["data"]
};
</script>
