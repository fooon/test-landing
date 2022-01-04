<template>
  <div class="title" :style="{ backgroundImage: url(imgSrc) }">
    {{ text }}
  </div>
</template>

<script>
export default {
  props: {
    text: String,
    imgSrc: String
  }
}
</script>

<style scoped>
.title{
  font-family: Anzeigen Grotesk T;
  font-style: normal;
  font-weight: 500;
  font-size: 64px;
  line-height: 51px;
  color: #FFFFFF;
  
  background-repeat: no-repeat;
  height: 100px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
}
</style>