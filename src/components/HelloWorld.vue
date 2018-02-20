<template>
  <div class="hello">
    <div id="header">
      <div id="box"></div>
      <div id="blog_title">
        MA<span>RIA</span> KX
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#header {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  background-image: url();
  background-position: center;
  background-repeat: repeat;
  background-size: cover;
  z-index: 100;
}

#box {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 75vh;
  height: 75vh;
  border: 10px solid var(--color-orange);
  -webkit-transform: translateX(-50%) translateY(-50%);
  -moz-transform: translateX(-50%) translateY(-50%);
  -ms-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}

#blog_title {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 80vw;
  font-family: Lato;
  font-size: 90px;
  color: #222222;
  line-height: 60px;
  letter-spacing: 2px;
  text-align: center;
  font-weight: bold;
  -webkit-transform: translateX(-50%) translateY(-50%);
  -moz-transform: translateX(-50%) translateY(-50%);
  -ms-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}

#blog_title span {
    color: var(--color-orange);
}
</style>
