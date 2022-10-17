<template>
<!-- Search Filter -->
          <div class="row filter-row">
            <div class="col-sm-6 col-md-3">  
              <div class="form-group form-focus">
                <input type="text" class="form-control floating">
                <label class="focus-label">Client ID</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3">  
              <div class="form-group form-focus">
                <input type="text" class="form-control floating">
                <label class="focus-label">Client Name</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3"> 
              <div class="form-group form-focus select-focus">
              <vue-select :options="addclientfilter" />
                <label class="focus-label">Company</label>
              </div>
            </div>
            <div class="col-sm-6 col-md-3">
              <div class="d-grid">
                <a href="#" class="btn btn-success"> Search </a>  
              </div>  
            </div>     
                    </div>
          <!-- Search Filter -->
</template>
<script>
  import Vue from 'vue'
  export default {
     data() {
    return {
      addclientfilter: ["Select Company", "Global Technologies", "Delta Infotech"]
    }
    },
    components: {
   
    },
    mounted() {
    }
  }
</Script>