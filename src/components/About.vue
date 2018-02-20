<template>
  <div id="about">
    <div id="about_panel">
      <div id="panelin">
        <div id="about_title">ABOUT MOI</div>

        <p><b>AGE</b> 26</p>
        <p><b>GENDER</b> FEMME (she/her) </p>
        <p><b>FROM</b> SPAIN, Madrid </p>
        <p><b>OCCUPATION</b> WEB DESIGNER </p>

        <div id="about_description">
          Life is too short. Don't waste time.
        </div>

      </div>
    </div>
    <div id="about_image"></div>

    <router-link :to="'/'">
      <div class="close">
          <span class="sf sf-cross-o"></span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'about'
}
</script>

<style>
#about {
  position: fixed;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  background: #ffffff;
  z-index: 10000;
  overflow: hidden;
}

#about_panel {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 50%;
  height: 100%;
  background-color: #ffffff;
  background-image: url();
  background-size: cover;
  z-index: 10000;
}

#panelin {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 280px;
  font-size: 12px;
  line-height: 20px;
  letter-spacing: 1px;
  text-align: right;
  color: #000000;
  -webkit-transform: translateX(-50%) translateY(-50%);
  -moz-transform: translateX(-50%) translateY(-50%);
  -ms-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}

#panelin b {
  float: left;
  color: var(--color-orange);
  letter-spacing: 2px;
  font-weight: 700;
}

#about_title {
  margin-top: 20px;
  margin-left: auto;
  margin-right: auto;
  font-size: 20px;
  line-height: 30px;
  font-weight: bold;
  text-align: center;
  text-transform: uppercase;
  color: #000000;
}

#about_description {
    margin: 20px auto;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: #000000;
}

#about_image {
  position: absolute;
    top: 0px;
    left: 50%;
    width: 50%;
    height: 100%;
    background-color: #000;
    background-image: url();
    background-size: cover;
    z-index: 10000;
}

</style>
