<template>
  <div class="advantages">
    <div class="title">ПРЕИМУЩЕСТВА НАШЕГО СЕРВИСА</div>
    <div class="items">
      <div
        class="item"
        v-for="(item, ix) in items"
        :key="ix"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
import titleBg from '../assets/title-bg-2.png'

export default {
  data(){
    return {
      items: [
        'Прокачаем вашу рефку в кратчайшие сроки',
        'Быстро и безопасно для вашего аккаунта',
        'Можно прокачать несколько рефералов',
        'Не нужно тратить уйму времени на прокачку реферала',
        'Забудь про автокликер'
      ],
      titleBg: titleBg
    }
  }
}
</script>

<style scoped>
.advantages{
  margin-bottom: 100px;
}
.title{
  font-family: Anzeigen Grotesk T;
  font-style: normal;
  font-weight: 500;
  font-size: 64px;
  line-height: 51px;
  color: #FFFFFF;
  
  background: url("../assets/title-bg-2.png") no-repeat;
  height: 100px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
  border-radius: 25px;
}

.items{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-column-gap: 49px;
}

.item{
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 130%;
  color: #B2ADFF;
  
  padding: 13px 20px;
  background: #1F1C4A;
  border-radius: 15px;
  min-height: 68px;
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
  
  .advantages{
    margin-bottom: 50px;
  }
}
</style>