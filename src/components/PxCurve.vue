<template>
  <svg class="Curve" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
    <path :fill="this.color" fill-opacity="1" d="M0,96L60,112C120,128,240,160,360,149.3C480,139,600,85,720,64C840,43,960,53,1080,64C1200,75,1320,85,1380,90.7L1440,96L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path>
  </svg>
</template>
<script>

export default{
  name: "px-curve",
  props: {
    color: String,
  },
  data(){
    return{
        
    }
  }
}
</script>
<style>
.Curve{
  margin-top: -15rem;
}
</style>