<template>
  <div class="how-its-work">
    <div class="title">КАК ЭТО РАБОТАЕТ?</div>
    <div class="items">
      <div
        class="item"
        v-for="(item, index) in items"
        :key="item.message"
      >
        <div class="text" v-html="item.title"></div>
        <div class="number">
          {{ index + 1 }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      items: [
        { title: 'Нажми на кнопку <a class="link" href="#">прокачать реферал</a>' },
        { title: 'Пройди короткую регистрацию в личном кабинете' },
        { title: 'Скопируй свою реферальную ссылку в игре' },
        { title: 'Добавь свою реферальную ссылку в личный кабинет и выбери категории прокачки' },
        { title: 'Наш бот автоматически делает прокачку абсолютно легальным образом' },
        { title: 'Жди получение подарков на свой аккаунт в течение нескольких дней.' },
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
  
  background: url("../assets/title-bg-3.png") no-repeat;
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
  grid-template-columns: 1fr 1fr 1fr;
}
.item{
  background-color: #1F1C4A;
  background-image: url("../assets/ellipse.png");
  background-position: right bottom;
  background-repeat: no-repeat;
  border-radius: 25px;
  padding: 24px 190px 24px 41px;
  //width: 547px;
  max-width: 547px;
  min-height: 184px;
  position: relative;
  margin: 0 20px 25px 0;
  overflow: hidden;
}
.number{
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 96px;
  line-height: 130%;
  
  color: #FFFFFF;
  position: absolute;
  right: 23px;
  bottom: -34px;
}
.text{
  font-family: Mabry Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 130%;
  color: #B2ADFF;
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
    height: 91px;
    min-height: 91px;
    margin: 0;
    max-width: 100%;
    background-size: 100px;
    padding: 10px 100px 10px 17px;
  }
  
  .text{
    font-size: 16px;
  }
  
  .number{
    font-size: 64px;
    right: 18px;
    bottom: -21px;
  }
}
</style>