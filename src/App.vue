<template>
  <div id="app">
    <Header  name="Mona"/>
    <Table  />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Table from  './components/Table.vue'
export default {
  name: 'App',
  components: {
    Header,
    Table,
  },
}
</script>

<style>
body{
 font-family: "Inv Maison Neue", "Maison Neue", -apple-system, BlinkMacSystemFont,'Open Sans',open-sans, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app {
  color:#9ca4ab;
}
table tr th{
  font-size: 12px;
  color: #9ca4ab;
  font-weight:500;
}
table tr td p {
  margin: 1px;
}
.table.b-table > thead > tr > [aria-sort]:not(.b-table-sort-icon-left), .table.b-table > tfoot > tr > [aria-sort]:not(.b-table-sort-icon-left) {
    background-position: right calc(0.75rem / 2) center;
    padding-right: calc(0.75rem + 0.65em);
    width: 33.33%;
}
</style>