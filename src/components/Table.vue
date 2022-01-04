<template>
    <table class="table  mytable" >
  <tbody>
    <tr>
        <td class="table_head">Cage Code<i class="bi bi-caret-up-fill"></i> <i class="bi bi-caret-down-fill"></i></td>
        <td class="table_head">Company</td>
        <td class="table_head">Description</td>
    </tr>

    <tr v-for="company in companies" :key="company.code">
      <td class="code">{{ company.code }}</td>
      <td>{{ company.name }}</td>
      <td>{{ company.discription }}</td>
    </tr>
  </tbody>
</table>

</template>

<script>
import '../../node_modules/bootstrap/dist/css/bootstrap.min.css'
export default {
    name:'Table',
    data(){
        return {
            companies:[
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
            ]
        }
    }
}
</script>

<style>
.mytable{
    width:96%;
    height:300px;
    margin:20px auto;
}

.table_head{
    font-size:12px;
    color:#9ca4ab;
}
.code{
    color:#2a9fd8;
    cursor:pointer;
}
</style>