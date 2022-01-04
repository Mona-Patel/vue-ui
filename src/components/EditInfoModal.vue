<template>
  <div>
    <b-modal v-model="showModal" id="modal-1" title="Edit Table" class="w-100">
      <p class="my-4">Hello from modal!</p>
      <p>Comments: {{ data.comments }}</p>
      <p>
        URL: <a :href="data.url">{{ data.url }}</a>
      </p>
      <div class="form-group">
        <label for="inputAddress">Address</label>
        <input type="text" class="form-control" id="inputAddress" placeholder="1234 Main St">
      </div>
    </b-modal>
  </div>
</template>

<script>
import { BModal } from "bootstrap-vue";
export default {
  // data() {
  //   return {
  //     data: "",
  //     showModal: "",
  //   };
  // },
  props: ["data", "showModal"],
  components: {
    "b-modal": BModal,
  },
  // mounted() {
  //   this.$root.$on("edit-table", (data) => {
  //     this.data = data.item;
  //   });
  // },
};
</script>

<style scoped>
div {
  margin: auto 0;
  width: 100%;
}
</style>