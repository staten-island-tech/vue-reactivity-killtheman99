<template>
  <div>
    <div class="topbar">
      <p>Cart</p>
      <Cart class="cart" :items="items" :total="total" />
    </div>
    <h1 class="ck">Vue Project</h1>
    <div class="box">
      <Fruit
        v-for="menu in menus"
        :key="menu"
        :img="menu.img"
        :name="menu.name"
        :price="menu.price"
        @button-clicked="add"
      />
    </div>
  </div>
</template>

<script>
import Fruit from './MenuItem.vue'
import Cart from './cart.vue'

export default {
  components: {
    Fruit,
    Cart
  },
  data() {
    return {
      items: 0,
      total: 0,
      menus: [
        {
          img: 'https://cdn.britannica.com/55/174255-050-526314B6/brown-Guernsey-cow.jpg',
          name: 'Her name is strawberry',
          price: 2
        },
        {
          img: 'https://images.immediate.co.uk/production/volatile/sites/30/2020/02/Glass-and-bottle-of-milk-fe0997a.jpg?resize=960,872',
          name: 'This is her Milk',
          price: 420
        },
        {
          img: 'https://www.thespruce.com/thmb/WHDh42dmxIiAg5YuTftvBrqLevk=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/zoysia-grass-plant-profile-4691117-hero-2c01933247654f5b8c694a49eb6fa7bc.jpg',
          name: 'This is her meal',
          price: 88
        },
        {
          img: 'https://media.istockphoto.com/id/1273939455/photo/portrait-of-a-bull-in-the-field.jpg?s=612x612&w=0&k=20&c=PhW7CLe5ZMTg6ltnc6DxMAlCW5gt99VqKZr5gBfbScI=',
          name: 'This is her boyfriend',
          price: 999
        }
      ]
    }
  },
  methods: {
    add() {
      this.items = this.items + 1
      this.total = this.total + this.price
    }
  }
}
</script>

<style scoped>
.topbar {
  height: 100px;
  width: 100%;
  position: absolute;
  display: flex;
  top: 0px;
  left: 0px;
  background-color: rgb(79, 83, 88);
  justify-content: right;
}

.ck {
  color: white;
  margin: auto;
  position: relative;
  display: block;
  margin-top: 25px;
  text-align: center;
  font-size: 50px;
}

.cart {
  margin-top: 20px;
  margin-right: 45px;
  position: relative;

}

.box {
  display: flex;
  flex-direction: row;

}
</style>
