<template>
  <div class="services">
    <div class="title">
      НАШИ УСЛУГИ
    </div>
    <div class="items">
      <div
        class="item"
        v-for="item in serviceItems"
        :key="item.text"
        :style="{ backgroundImage: 'url(' + item.bg + ')' }"
      >
        <div class="service-title" :style="{ backgroundColor: item.titleColor }">
          {{ item.title }}
        </div>
        <br />
        <div
          v-for="label in item.labels"
          class="label-item"
          :key="label.text"
          :style="label.style"
        >
          <img :src="label.icon" alt="">
          <div class="label">{{ label.text }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import energyIcon from '../assets/icons/energy.svg';
import epicBookIcon from '../assets/icons/epic-book.svg';
import sacralisIcon from '../assets/icons/sacralis.svg';
import xpIcon from '../assets/icons/xp.svg';
import voidShard from '../assets/icons/void-shard.svg';

import sticker1 from '../assets/stickers/sticker-1.png'
import sticker2 from '../assets/stickers/sticker-2.png'
import sticker3 from '../assets/stickers/sticker-3.png'

export default {
  data(){
    return {
      serviceItems: [
        {
          title: 'ПРОКАЧКА HARD ЗА 999₽',
          titleColor: '#5A0CFF',
          labels: [
            { text: '4 сакрала', icon: sacralisIcon },
            { text: '3 войд осколка', icon: voidShard },
            { text: '6 древних книг', icon: epicBookIcon },
            { text: '3 XP', icon: xpIcon },
            { text: '600 энергии', icon: energyIcon },
          ],
          bg: sticker1
        },
        {
          title: 'ПРОКАЧКА MEDIUM ЗА 666₽',
          titleColor: '#B338FF',
          labels: [
            { text: '2 сакрала', icon: sacralisIcon },
            { text: '2 войд осколка', icon: voidShard },
            { text: '400 энергии', icon: energyIcon },
            { text: '4 эпические книги', icon: epicBookIcon },
            { text: '2 XP', icon: xpIcon },
          ],
          bg: sticker2
        },
        {
          title: 'ПРОКАЧКА SOFT ЗА 333₽',
          titleColor: '#F048FF',
          labels: [
            { text: '1 сакрал', icon: sacralisIcon },
            { text: '1 войд осколок', icon: voidShard },
            { text: '200 энергии', icon: energyIcon, style: { marginRight: 0 } },
            { text: '2 эпические книги', icon: epicBookIcon },
            { text: '3 XP на 3 дня', icon: xpIcon },
          ],
          bg: sticker3
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.title{
  font-family: Anzeigen Grotesk T;
  font-style: normal;
  font-weight: 500;
  font-size: 64px;
  line-height: 51px;
  color: #FFFFFF;
  
  background: url("../assets/title-services-bg.png");
  height: 100px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 25px;
  margin-bottom: 25px;
}

.items{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 19px;
  margin-bottom: 100px;
}

.item{
  min-height: 184px;
  padding: 28px 40px;
  background: #1F1C4A;
  background-position: right bottom;
  background-repeat: no-repeat;
  border-radius: 25px;
  
  .service-title{
    font-family: Anzeigen Grotesk T;
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    line-height: 16px;
    color: #FFFFFF;
    
    padding: 7px 15px;
    display: inline-flex;
    border-radius: 5px;
    height: 30px;
    margin-bottom: 26px;
  }
  
  .label-item{
    display: inline-flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 12px;
    margin-right: 5px;
    img{
      width: 32px;
      height: 32px;
    }
  }
  
  .label{
    font-family: Anzeigen Grotesk T;
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    line-height: 16px;
    color: #B2ADFF;
    
    padding: 7px 15px;
    background: #292563;
    border-radius: 5px;
    display: inline-flex;
    margin-left: 6px;
  }
}

@media(max-width: 768px) {
  .title{
    font-size: 24px;
    line-height: 19px;
    height: 40px;
    background-size: cover;
  }
  
  .items{
    grid-template-columns: 1fr;
    grid-row-gap: 25px;
    margin-bottom: 50px;
  }
  
  .item{
    padding: 25px 17px;
  }
}
</style>