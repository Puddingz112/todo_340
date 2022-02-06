<template>
  <v-container>
    <Data @Input="validate"></Data>
    <Table :desserts="desserts"></Table>
  </v-container>
</template>

<script>
import Data from "../components/Data.vue";
import Table from "../components/Table.vue";
export default {
  data: () => ({
    desserts: [],
  }),
  desserts: "Input",
  methods: {
    validate(select, name) {
      this.desserts.push({
        name: select + " : " + name,
      });
    },
  },
  components: { Data, Table },
};
</script>

<style></style>
