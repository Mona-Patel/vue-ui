<template>
    <div class="header">
        <nav>
            <div class="header_content">
                <div class="input_box">
                    <span>Filter by Text</span>
                    <input type="text" class="login" placeholder="Enter Text" id="search">
                </div>
                
                <div class="input_box">
                    <span>Filter by Company Name</span>
                    <select class="form-select" aria-label="Default select example" id="selectbox">
                        <option selected>All Roles</option>
                        <option v-for="company in companies" :key="company.code">{{ company.name }}</option>
                    </select>
                </div>
                <div class="button">
                    <button class="btn btn-outline-primary me-md-2 mt-4 px-4" type="button" v-on:click="reset">Reset</button>
                    <button class="btn btn-primary mt-4 px-4" type="button">Filter</button>
                </div>


                <div class="button2">
                    <button class="btn btn-outline-primary me-md-2 mt-4 download" type="button">Download All</button>
                    <button class="btn btn-primary mt-4 px-4 download2" type="button" v-b-modal.modal-center>Add New Cage Code</button>
                </div>
                <b-modal id="modal-center"  title="Add Cage Code">
                      <p class="my-4">Content goes here...</p>
                 </b-modal>
            </div>
        </nav>
    </div>
</template>

<script>
import '../../node_modules/bootstrap/dist/css/bootstrap.min.css'
export default {
    name:'Header',
    props:{
        name:String
    },
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
    },
   methods:{
       reset:function(){
           document.querySelector('#search').value='';
           document.querySelector('#selectbox').value='All Roles';
       }
   }
}
</script>

<style>
.header{
    width:100%;
    box-sizing:border-box;
    background:white;
    display:flex;
    height:65px;
}
.header_content{
    display: flex;
    justify-content:space-around;
    align-items:center;
    padding-left:20px;
    width:100%;
}
.input_box {
    width: 50%;
    margin-right: 20px;
}
.input_box > input[type=text]{
    width: 338px;
}
.login {
    border: 0;
    outline: 0;
    background: transparent;
    border-bottom: 1px solid #9ca4ab;
}
::placeholder{
    padding-left: 10px;
    color:#D3D3D3;
    font-weight:200;
}

span{
    font-size:12px;
    color:#9ca4ab;
    padding:15px 0px;
}

.button{
    display: flex;
    justify-content:center;
    align-items:start;
}

.button2{
    display: flex;
    justify-content: end;
    align-items: center;
    width: 72%;
    height: 65px;
    padding-left: 167px;
}
.download{
    width:122px;
}
.download2{
  width: 201px;
}
</style>