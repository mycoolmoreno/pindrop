<template>
     <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #3399C1;box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.25);">
    <div class="container">
      <a class="navbar-brand nav-lt" href="../index.html">
        <img src="https://assets.codepen.io/3904500/pindrop-logo.svg" />
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

      <div class="collapse navbar-collapse right vrt-aln-ctr" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link nav-lt" href="../index.html">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link nav-lt" href="#">About</a>
          </li>

        </ul>
      </div>
    </div>
  </nav>


</template>

<script>

</script>

<style scoped>

/* || Navigation Styles */

.nav-lt {
  color: white !important;
  font-size: 18px;
  line-height: 28px;
  align-items: center;
  font-weight: 600px;
  font-style: normal;
  font-family: "sofia-pro";
}

.nav-cta {
  color: #3399C1 !important;
  background: #FFFFFF;
  border: 2px solid #3399C1;
  box-sizing: border-box;
  border-radius: 12px;
  padding: 5px 20px !important;
  line-height: 22px;
  font-family: "sofia-pro";
  font-style: normal;
  font-size: 14px;
  font-weight: bold;
  text-transform: uppercase;
  align-items: center;
  padding: 8px 32px;
  text-align: center;
  margin-left: 30px;
  margin-top: auto;
  margin-bottom: auto;
}

.nav-cta:hover {
  background-color: #EEE;
}



.vrt-aln-ctr {
  display: flex;
  align-items: center;
}


</style>