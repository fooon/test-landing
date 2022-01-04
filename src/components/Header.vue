<template>
  <div class="header">
    <img class="desktop-bg" src="../assets/header-inner.png" alt="1">
    <img class="mobile-bg" src="../assets/mobile-head-inner.png" alt="1">
    <div class="text">
      ПРОКАЧАЙ СВОЙ РЕФЕРАЛ В ОДИН КЛИК
    </div>
    <div class="button">
      ПРОКАЧАТЬ РЕФЕРАЛ
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.header{
  /*padding: 0 6.25%;*/
  display: flex;
  flex-direction: column;
}
.mobile-bg{
  display: none;
}
.text{
  font-family: Anzeigen Grotesk T;
  font-style: normal;
  font-weight: 500;
  font-size: 64px;
  line-height: 51px;
  color: #FFFFFF;
  
  text-align: center;
  margin-top: 35px;
}
.button{
  background: #A30CFF;
  border-radius: 15px;
  display: inline-flex;
  margin: 25px auto 100px;
  align-items: center;
  justify-content: center;
  width: 372px;
  height: 83px;
  cursor: pointer;
  user-select: none;
  
  border: 3px solid;
  border-image-source: linear-gradient(267.19deg, #CA69FF 1.48%, rgba(255, 255, 255, 0) 16.87%, rgba(255, 255, 255, 0) 82.26%, #EB9AFF 98.06%);
  
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 24px;
  color: #FFFFFF;
  
  &:hover{
    background: #b035fb;
  }
  &:active{
    background: #8a0dd7;
  }
}

@media(max-width: 768px){
  .text{
    font-size: 24px;
    line-height: 19px;
  }
  .button{
    width: 183px;
    height: 59px;
    font-size: 14px;
    line-height: 14px;
    margin-bottom: 50px;
  }
  
  .mobile-bg{
    display: block;
  }
  .desktop-bg{
    display: none;
  }
}

</style>