<template>

<div class="container mix-container app-main" id="MixItUp0EF6FE">
    <div class="row">
      <div class="col-12 col-md-7 col-lg-6 order-md-1" id="questions">
        <h3 style="padding-left:0px !important;">  Filter your results. </h3>
        
        <form class="controls">
          <button type="reset" class="btn btn-outline-secondary control control-text btn-state-reverse">Reset</button>

          <div class="question-card">
          <h4> Regions </h4>
          <fieldset data-filter-group class="checkbox-group">
            <div class="checkbox">
              <input type="checkbox" value=".nw" />
              <label class="checkbox-label">North West:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".w" />
              <label class="checkbox-label">West:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".sw" />
              <label class="checkbox-label">South West:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".mw" />
              <label class="checkbox-label">Mid-West:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".ne" />
              <label class="checkbox-label">North East:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".ma" />
              <label class="checkbox-label">Mid-Atlantic:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".se" />
              <label class="checkbox-label">South East:</label>
              
            </div>
          </fieldset>
          </div>
          <div class="question-card">
          <h4> Other Factors </h4>
          <fieldset data-filter-group class="checkbox-group">
            <div class="checkbox">
              <input type="checkbox" value=".kids" />
              <label class="checkbox-label">Kid Friendly:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".dogs" />
              <label class="checkbox-label">Dog Friendly:</label>
              
            </div>

            <div class="checkbox">
              <input type="checkbox" value=".foodie" />
              <label class="checkbox-label">Foodie Friendly:</label>
              
            </div>
            
            <div class="checkbox">
              <input type="checkbox" value=".low-cost" />
              <label class="checkbox-label">Low Cost of Living:</label>
              
            </div>
            
            <div class="checkbox">
              <input type="checkbox" value=".outdoors" />
              <label class="checkbox-label">Outdoors Friendly:</label>
              
            </div>
            
            <div class="checkbox">
              <input type="checkbox" value=".tech" />
              <label class="checkbox-label">Tech Hub:</label>
              
            </div>
            
            
          </fieldset>
          </div>
          
        </form>
      </div>
      <div class="col-12 col-md-5 col-lg-6 order-md-2" id="app">
        <div class="container mix-container">
          <h3 style="padding-left:0px !important;"> Explore your options.</h3>
          <div class="row row-cols-1 row-cols-md-1" style="">
            <div v-for="destination in destinations"  class="col mb-4 mix" :key="destination.name" :class="destination.filters">
              <div class="card">
                <img :src="destination.image" class="card-img-top" alt="...">
                <div class="card-body">
                  <h5 class="card-title">{{ destination.name }}</h5>
                  <p class="card-text">{{ destination.description }}</p>
                  <router-link :to="{name: 'DestinationsDetails', params: {slug:destination.slug}}" class="btn btn-primary btn-state-default "> Explore </router-link>
                  
                </div>
              </div>

            </div>
          </div>

        </div>

      </div>
    </div>
  </div>

</template>


<script>
import store from "@/store.js"


export default {
  name: "Home",
  components: {
    
  },
  data(){
    return {
      destinations: store.destinations
    }
  }
};
</script>


<style scoped>
#questions {
  background-color: white;
    min-height: 600px;
    border: 1px solid lightgray;
    padding: 20px;
}

#app {
    background-color: lightgray;
    height: 1000px;
    padding: 20px;
    overflow: scroll;
    border: 1px solid lightgray;
}

.card {
     text-align: left;
}


h3 {
    font-size: 20px;
    font-weight: bold;
    padding: 20px;
    padding-left: 0px !important;
    text-align: left;
}

.question-card {
    text-align: left;
}

.checkbox label {
    margin-left: 10px;
}


/* || Button Styles */

.btn-state-default {
  background: #3399C1 !important;
  border-radius: 12px;
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 37px;
  /* display: flex; */
  align-items: center;
  text-align: center;
  text-transform: uppercase;
  color: #FFFFFF;
  border: 1px solid #3399C1 !important;
  }

a.btn-state-default:active {
  background: #838D92 !important;
  border-color: #838D92 !important;
}

.btn-state-default:hover {
  background: #568FA6!important;
  border-color: #568FA6 !important;
}

a.btn-state-disabled {
  background: #E8ECEE;
  border-radius: 12px;
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 37px;
  display: flex;
  align-items: center;
  text-align: center;
  text-transform: uppercase;
  color: #FFFFFF;
  
}

.btn-state-reverse {
  background: #FFFFFF !important;
  border: 2px solid #3399C1 !important;
  box-sizing: border-box;
  border-radius: 12px;
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 37px;
  display: flex;
  align-items: center;
  text-align: center;
  text-transform: uppercase;
  color: #3399C1 !important;
}

.btn-state-reverse:hover {
  background: #E8ECEE !important;
  color: #3399C1 !important;
  border: 2px solid #3399C1 !important;
}

.btn-state-reverse:active {
  background: #838D92 !important;
  color: #FFF !important;
  border: 2px solid #3399C1 !important;
}


.filters {
  background-color: #e2e2e2;
  height: 400px;
  display: flex;
  justify-content: center;
  padding-top: 15px;
  padding-bottom: 15px;
  margin-bottom: 30px;
}

.controls {
  align-items: center;
}

#questions {
  background-color: white;
  min-height: 600px;
  border: 1px solid lightgray;
  padding: 20px;
/*   border-top-left-radius: 14px; */
}

#questions h3 {
  font-size: 20px;
  font-weight: bold;
  padding: 20px 20px 20px 0px;
}

#results {
  background-color: lightgray;
  height: 1000px;
  padding: 20px;
  overflow: scroll;
  border: 1px solid lightgray;
/*   border-top-right-radius: 14px; */
}

#app::-webkit-scrollbar {
  display: none;
}

#results h3 {
  font-size: 20px;
  font-weight: bold;
  padding: 20px;
}

/* .controls {
  padding-left: 20px;
} */

.controls h4 {
  margin-top: 20px;
  font-size: 20px;
}

.intro-container {
  max-width: 960px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
  margin-bottom: 40px;
}

.app-main {
  margin-top: 20px;
}

.explore-city-btn {
  background: #3399C1 !important;
  border-radius: 12px;
  border: 1px solid #3399C1 !important;
  
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 25px;
  /* identical to box height */

  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: #FFFFFF;
}

.question-card {
  border: 1px solid #999999;
  border-radius: 14px;
  padding: 10px;
  margin: 15px 0px;
  padding-left: 15px;
}


#emptystate {
  visibility: visible;
  padding-left: 15px;
}


</style>