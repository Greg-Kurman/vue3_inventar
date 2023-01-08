<template>
  <div class="wrapper">
    <div class="main">
      <div class="inventar">
        <div class="inventar_body">
          <div class="inventar_body__left">
            <img src="../assets/blur.png" alt="">
            <div class="sk1"></div>
            <div class="sk2"></div>
            <div class="sk3"></div>
            <div class="sk4"></div>
            <div class="sk5"></div>
            <div class="sk6"></div>
            <div class="sk7"></div>
          </div>
          <div class="inventar_body__right">
            <div class="body_inner__right">

              <MyModal v-bind:open="this.open" v-on:openM="openMod()" />
              <MyItem @:click="openMod()" v-for="item in items" v-bind:color="item.color" v-bind:key="item.id" v-bind:count="item.count" />


            </div>
          </div>
        </div>
        <div class="inventar_footer">
          <div class="inventar_footer__ghost">
          </div>
          <a href=""><img src="../assets/Vector.png" alt=""></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MyItem from './MyItem.vue'
import MyModal from './MyModal.vue'

export default {
  components: {
    MyItem,
    MyModal
  },
  name: 'MyInventar',

  data() {
    return {
      open: false,
      items: [
        {
          id:1,
          color: 'red',
          count: 5
        },
        {
          id:2,
          color: 'green',
          count: 2
        },
        {
          id:3,
          color: 'purple',
          count: 3
        }
      ]

    }
  },
  props: {
  },
  methods: {
    openMod: function () {
      console.log('hi')
      console.log(this.open)
      this.open = !this.open
      console.log(this.open)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.wrapper {
  height: 100vh;

}

.inventar {
  padding-top: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 100;
}

.inventar_body {
  display: flex;
  margin-bottom: 24px;
  z-index: 30;
  overflow: hidden;
}

.inventar_body__left {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-right: 24px;
  width: 236px;
  height: 500px;
  background: #262626;
  border: 1px solid #4D4D4D;
  border-radius: 12px;
}

.inventar_body__left img {
  margin-top: 18px;
  width: 208px;
  height: 240px;
}

.sk1 {
  margin: 20px 0 24px 0;
  width: 190px;
  height: 26px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 8px;
}

.sk2 {
  margin-bottom: 16px;
  width: 155px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.sk3 {
  margin: 16px;
  width: 190px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.sk4 {
  margin: 16px;
  width: 170px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.sk5 {
  margin: 16px;
  width: 160px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.sk6 {
  margin: 16px;
  width: 140px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.sk7 {
  margin: 24px;
  width: 80px;
  height: 10px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 4px;
}

.inventar_body__right {
  position: relative;
  background-image: url("../assets/Row.png");
  width: 525px;
  height: 500px;
  border: 1px solid #4D4D4D;
  border-radius: 12px;
}

.body_inner__right {
  position: absolute;
  display: flex;
  flex-direction: column-reverse;
  flex-wrap: wrap;
  top: -25px;
  right: 12px;
  background-image: url("../assets/Row.png");
  width: 500px;
  height: 525px;
  -webkit-transform: rotate(90deg);
  -moz-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  -o-transform: rotate(90deg);
  transform: rotate(90deg);

}

.inventar_item {
  width: 105px;
  height: 100px;
  border: 1px solid #4D4D4D;
}

.inventar_footer {
  display: flex;

  width: 785px;
  height: 72px;
  background: #262626;
  border: 1px solid #4D4D4D;
  border-radius: 12px;
}

.inventar_footer a {
  margin: 14px 0 0 22px;
}

.inventar_footer__ghost {
  margin: 18px;
  width: 699px;
  height: 36px;
  background: linear-gradient(90deg, #3C3C3C 0%, #444444 51.04%, #333333 100%);
  border-radius: 12px;
}
</style>
