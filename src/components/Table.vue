<template>
  <div id="app" class="overflow-auto">
    <b-table
      class="table"
      :items="items"
      thead-class=" text-gray font-3"
      :fields="tableFields"
      :label-sort-asc="tableLabelSortAsc"
      per-page="9"
      :current-page="currentPage"
    >
      <template #cell(view)="data">
        <a target="_blank" rel="noopener" class="no-link" :href="data.item.url">
          <b-icon icon="eye-fill" />
        </a>
      </template>
      <template #cell(edit)="data" class="code_section heading">
        <p @click.prevent="editTable(data)" class="para">{{data.item.code}}</p>
      </template>
    </b-table>
    <div>
      <b-pagination v-model="currentPage" :total-rows="rows" size="sm" :per-page="5"
      :current-page="currentPage" align="right"></b-pagination>
    </div>
    <edit-info-modal :data="data" :showModal="showModal" />
  </div>
</template>

<script>
import { BIcon, BTable,BPagination } from "bootstrap-vue";
import EditInfoModal from "./EditInfoModal.vue";
export default {
  name: "Table",
  components: {
    "b-table": BTable,
    "b-icon": BIcon,
    "b-pagination":BPagination,
    "edit-info-modal": EditInfoModal,
  },
  data() {
    return {
      rows: 15,
      currentPage: 1,
      tableBordered: true,
      tableLabelSortAsc: "",
      tableFields: [
        { sortable: true,  key: "edit", label: "Cage Code"},
        { sortable: true,  key: "name", label: "Company Name" },
        { sortable: true,  key: "discription", label: "Description" },
      ],
      items: [
           {
                    code:12335,
                    name:'Tech Mahindra',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12336,
                    name:'Capgemini',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                 {
                    code:12337,
                    name:'TCS',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },

                 {
                    code:12338,
                    name:'Infosys',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                 {
                    code:12339,
                    name:'Wipro',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },

                 {
                    code:12340,
                    name:'AppZoy',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                 {
                    code:12341,
                    name:'HCL Technologies',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                 {
                    code:12342,
                    name:'Mphasis',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                 {
                    code:12343,
                    name:'Redington',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },

                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },
                {
                    code:12344,
                    name:'Larsen and Tourbo',
                    discription:'Service based company',
                    address:'jaipee Nagar karnataka',
                    city:'Bangalore',
                    state:'Karnataka',
                    zipcode:'455001',
                    country:'india',
                    location_code:'12345',
                    ge_source_code:'NA',
                    Region:'-',
                    vendor:'-'
                },



      ],
      data: "",
      showModal: false,
    };
  },
  methods: {
    editTable(data) {
     console.log("data",data.item.code);
      this.data = Object.assign({}, data.item.code);
      this.showModal = true;
    },
  }
};
</script>

<style scoped>
.table{
    width:96%;
    height:300px;
    margin:40px auto;
}
.para{
    cursor: pointer;
    color:#2a9fd8;
}
.code_section{
    width:33%;
}
.my_heading{
  color:#9ca4ab!important;
  font-size:20px !important;;
}
</style>