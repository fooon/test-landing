<template>
  <div class="footer">
    <div class="title">ПОЧЕМУ НАМ СТОИТ ДОВЕРЯТЬ?</div>
    <div class="items">
      <div
        class="item"
        v-for="item in items"
        :key="item.text"
      >
        <div class="text">
          {{ item.text }}
        </div>
        <img :src="item.bg" :alt="item.bg" class="bg">
      </div>
    </div>
    <div class="questions">
      По любым вопросам или проблемам вы можете обратиться в службу поддержки пользователей. Мы с радостью ответим на любые вопросы!
    </div>
    <div class="help-button">
      НАПИСАТЬ В СЛУЖБУ ПОДДЕРЖКИ
    </div>
  </div>
</template>

<script>
import img1 from '../assets/sticker-1.png';
import img2 from '../assets/sticker-2.png';
import img3 from '../assets/sticker-3.png';
import img4 from '../assets/sticker-4.png';

export default {
  data(){
    return {
      items: [
        { 
          text: "Мы не просим у вас данные от входа в аккаунт", 
          bg: img1
        },
        { 
          text: "Мы сотрудничаем с крупными блогерами",
          bg: img2
        },
        { 
          text: "Нашим сервисом пользуются более 40 тысяч человек в игре Raid.",
          bg: img3
        },
        { 
          text: "Наши отзывы",
          bg: img4
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.footer{
  margin-top: 75px;
  padding-bottom: 141px;
}

.items{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
.title{
  font-family: Anzeigen Grotesk T;
  font-style: normal;
  font-weight: 500;
  font-size: 64px;
  line-height: 51px;
  color: #FFFFFF;
  
  background: url("../assets/title-footer-bg.png") no-repeat;
  height: 100px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
}
.item{
  background: #1F1C4A;
  border-radius: 25px;
  min-height: 103px;
  max-width: 369px;
  margin: 0 69px 0 0;
  position: relative;
  padding: 22px 81px 22px 32px;
  overflow: hidden;
  
  .bg{
    position: absolute;
    right: 0;
    bottom: 0;
  }
  
  .text{
    font-family: Mabry Pro;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 130%;
    color: #B2ADFF;
  }
}
.questions{
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: normal;
  font-size: 36px;
  line-height: 130%;
  text-align: center;
  color: #FFFFFF;
  margin-top: 140px;
}
.help-button{
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 24px;
  color: #FFFFFF;
  
  width: 547px;
  height: 83px;
  background: #A30CFF;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  margin: 25px auto 0;
  user-select: none;
  
  border: 3px solid;
  border-image-source: linear-gradient(267.19deg, #CA69FF 1.48%, rgba(255, 255, 255, 0) 16.87%, rgba(255, 255, 255, 0) 82.26%, #EB9AFF 98.06%);
  
  &:hover{
    background: #b035fb;
  }
  &:active{
    background: #8a0dd7;
  }
}


@media(max-width: 768px) {
  .title{
    font-size: 24px;
    line-height: 19px;
    height: 40px;
  }
  
  .items{
    grid-template-columns: 1fr;
    grid-row-gap: 25px;
  }
  
  .item{
    min-height: 91px;
    margin: 0;
    max-width: 100%;
    padding: 16px 81px 16px 32px;
    display: inline-flex;
    align-items: center;
  }
  
  .footer{
    margin-top: 50px;
    padding-bottom: 50px;
  }
  
  .questions{
    margin-top: 50px;
    font-size: 16px;
  }
  
  .help-button{
    width: 327px;
    height: 66px;
    font-size: 16px;
  }
}
</style>