<template>
    <main role="main" class="main main-content">

    <section class="hero-banner" style="background-color: #FFF;">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-12 col-md-7 col-lg-6 order-md-1 aos-init aos-animate">
          <h1 class="display-4 font-weight-normal hero-banner-content hero-header" style="margin-left: 0 !important">Pin marks the spot.</h1>
        <p class="lead font-weight-normal hero-subheader" style="margin-left: 0 !important">Finding the perfect place to live is hard. PinDrop gives you the information you need to drop your pin with confidence.</p>
        <router-link :to="{name: 'CitySearch'}" class="btn btn-outline-secondary main-cta" style="margin-left: 0 !important">Get Started</router-link>
        </div>
        <div class="col-12 col-md-5 col-lg-6 order-md-2" style="margin-top: 15px;">
          <img src="https://assets.codepen.io/3904500/hero-image.png" class="img-fluid mw-md-150 mw-lg-130 mb-6 mb-md-0 aos-init aos-animate" />
        </div>
        
      </div>
    </div>
  </section>
    
 

    <div class="container marketing">
      <h2 class="main-sec-intro">How it works.</h2>
      <p> Find the perfect place for you in three simple steps.</p>
      <br>
      <!-- Three columns of text below the carousel -->
      <div class="row all-steps">
        <div class="col-lg-4 steps">
         
          <p class="large-num left-align"> 1 </p>
          <h2 class="left-align">Figure it out</h2>
          <hr style="width: 50px;border-width: 2px;text-align:left;margin-left:0;">
          <p class="left-align">First, use our filtering system to find a city that fits you and your family.</p>
          <p class="left-align">
              <router-link :to="{name: 'CitySearch'}" class="sec-cta" role="button">Get Moving</router-link>
          </p> 
        </div>
        <!-- /.col-lg-4 -->
        <div class="col-lg-4 steps">
          
          <p class="large-num left-align"> 2 </p>
          <h2 class="left-align">Pick a City</h2>
          <hr class="left-align" style="width: 50px;border-width: 2px;text-align:left;margin-left:0;">
          <p class="left-align">Once we're on the same page, we'll give you a list of city options that fit you best.</p>

        </div>
        <!-- /.col-lg-4 -->
        <div class="col-lg-4 steps">
         
          <p class="large-num left-align"> 3 </p>
          <h2 class="left-align">Choose Your Neighborhood</h2>
          <hr class="left-align" style="width: 50px;border-width: 2px;text-align:left;margin-left:0;">
          <p class="left-align">When you've settled on a city, explore it's neighborhoods and find the perfect living space with Zillow.com. Welcome home! </p>

        </div>
        <!-- /.col-lg-4 -->
      </div>
      <!-- /.row -->

      <!-- /END THE FEATURETTES -->

    </div>
    <!-- /.container -->

  </main>
</template>

<style scoped>

.main {
  text-align: left;
}


/* || Hero Banner Styles */

.hero-banner {
  padding-top: 50px;
  padding-bottom: 50px;
}

.hero-header {
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 48px;
  line-height: 56px;
  display: flex;
  align-items: center;

  color: #454D58;
  flex: none;
  order: 0;
  align-self: center;
  margin: 0px 16px;
  margin-bottom: 16px;
}

.hero-subheader {
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 21px;
  display: flex;
  align-items: center;

  color: #454D58;
  flex: none;
  order: 1;
  align-self: flex-start;
  margin: 0px 16px;
  margin-bottom: 30px;
}




/* || Landing Page Styles */

.main-cta {
  font-family: "sofia-pro";
  text-transform: uppercase;
  align-items: center;
  color: #FFFFFF;
  background-color: #3399C1;
  font-size: 16px;
  font-weight: bold;
  font-style: normal;
  padding: 7px 25px;
  border-radius: 12px;
/*   display: flex; */
  align-items: center;
  max-width: 175px;
  border: 1px solid #3399C1;
  margin-left: 16px;
}

.main-cta:hover {
  background-color: white;
  color: #3399C1;
  border: 1px solid #3399C1;
}

.large-num {

  font-style: normal;
  font-weight: 800;
  font-size: 96px;
  line-height: 149px;
  /* identical to box height */

  display: flex;
  align-items: center;

  color: #4A555A;


  /* Inside Auto Layout */

  flex: none;
  order: 0;
  align-self: flex-start;
  margin: 0px 8px;
}

.sec-cta {
  color: #3399C1;
  text-decoration: underline;
  font-weight: bold;
}

.main-content {
  background-color: #e2f1f8;
}

.main-sec-intro {
  margin-top: 56px;
  
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 31px;
  /* identical to box height */

  display: flex;
  align-items: center;

  color: #4A555A;
}

p.marketing {
  font-family: "sofia-pro";
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 25px;
  /* identical to box height */

  display: flex;
  align-items: center;

  color: #4A555A;
}

.left-align {
  text-align: left;
  margin-left: 0 !important;
}



.steps h2 {
  font-style: normal;
  font-weight: 800;
  font-size: 20px;
  line-height: 31px;
  /* identical to box height */

  display: flex;
  align-items: center;

  color: #4A555A;


  /* Inside Auto Layout */

  flex: none;
  order: 1;
  align-self: flex-start;
  margin: 0px 8px;
}

.hero-banner-content {
  text-align: left;
}

.hero-banner {
  margin: 0 !important;
}

</style>