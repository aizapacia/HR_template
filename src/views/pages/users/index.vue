<template>
  <div class="users">
    <div class="main-wrapper">
      <main-header></main-header>

       <sidebar></sidebar>
       <!-- Page Wrapper -->
       <div class="page-wrapper">
      
        <!-- Page Content -->
        <div class="content container-fluid">
        
          <!-- Page Header -->
          <div class="page-header">
            <div class="row align-items-center">
              <div class="col">
                <h3 class="page-title">Users</h3>
                <ul class="breadcrumb">
                  <li class="breadcrumb-item"><router-link to="/index">Dashboard</router-link></li>
                  <li class="breadcrumb-item active">Users</li>
                </ul>
              </div>
              <div class="col-auto float-end ms-auto">
                <a href="#" class="btn add-btn" data-bs-toggle="modal" data-bs-target="#add_user"><i class="fa fa-plus"></i> Add User</a>
              </div>
            </div>
          </div>
          <!-- /Page Header -->
          
          <!-- Search Filter -->
          <div class="row filter-row">
            <div class="col-sm-6 col-md-3">  
              <div class="form-group form-focus">
                <input type="text" class="form-control floating">
                <label class="focus-label">Name</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3"> 
              <div class="form-group form-focus select-focus">
                <vue-select :options="usercompany" />
                <label class="focus-label">Company</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3"> 
              <div class="form-group form-focus select-focus">
                <vue-select :options="userroll" />
                <label class="focus-label">Role</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3">  
              <a href="#" class="btn btn-success w-100"> Search </a>  
            </div> 
                
          </div>
          <!-- /Search Filter -->
          
          <usertable />

        </div>
        <!-- /Page Content -->
        
        <usermodal />
        
      </div>
      <!-- /Page Wrapper -->
    </div>
  </div>
</template>
<script>
  import Vue from 'vue'
  export default {
    components: {  
    },
    data() {
    return {
      usercompany: ["Select Company", "Global Technologies", "Delta Infotech"],
      userroll: ["Select Roll", "Web Developer", "Web Designer", "Android Developer", "Ios Developer"]
    }
    },
    mounted() {
    },
    name: 'users'
  }
</Script>