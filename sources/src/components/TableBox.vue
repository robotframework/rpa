<template>
  <div class="row">
       <div class="col table-responsive p-5">
         <b-table :items="items" :fields="fields"></b-table>
       </div>
  </div>
</template>

<script>
export default {
  props: ["data"],
  data() {
    return {
      items: this.data.rows,
      fields: this.data.fields
    };
  }
};
</script>
