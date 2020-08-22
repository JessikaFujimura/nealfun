<template>
  <div class="section">
    <div class="board">
        <img alt="billgates" src="../../src/assets/billgates.jpg">
        {{ text }}
    </div>
    <Total v-bind:total="total" />
    <div class="listItens">
      <Card 
              v-for="item in itens"
              v-bind:key="item.name"
              v-bind:name="item.name"
              v-bind:price="item.price"
              v-bind:photo="item.photo"
              @sell-change="sellItem(item)"
              @buy-change="buyItem(item)"
          >
      </Card>
    </div>
  </div>
</template>

<script>
import Total from './Total.vue'
import Card from './Card'

export default {
  name: 'Section',
  props: {
    text: String
  },
  components:{
      Total,
      Card
  },
   methods: {
        sellItem(item){
            this.total = this.total + item.price
        },
        buyItem(item){
            this.total = this.total - item.price
        },
    },
    data() {
      return  {
        total: 1000000000,
        itens: [
    {
        "name": "Big Mac",
        "price": 2,
        "photo": 'https://neal.fun/spend/images/big-mac.jpg'
    },
    {
        "name": "Flip Flops",
        "price": 3,
        "photo": "https://neal.fun/spend/images/flip-flops.jpg"
    },
    {
        "name": "Coca-Cola Pack",
        "price": 5,
        "photo": "https://neal.fun/spend/images/coca-cola-pack.jpg"
    },
    {
        "name": "Movie Ticket",
        "price": 12,
        "photo": "https://neal.fun/spend/images/movie-ticket.jpg"
    },
    {
        "name": "Book",
        "price": 15,
        "photo": "https://neal.fun/spend/images/book.jpg"
    },
    {
        "name": "Lobster Dinner",
        "price": 45,
        "photo": "https://neal.fun/spend/images/lobster-dinner.jpg"
    },
    {
        "name": "Video Game",
        "price": 60,
        "photo": "https://neal.fun/spend/images/video-game.jpg"
    },
    {
        "name": "Amazon Echo",
        "price": 99,
        "photo": "https://neal.fun/spend/images/amazon-echo.jpg"
    },
    {
        "name": "Year of Netflix",
        "price": 100,
        "photo": "https://neal.fun/spend/images/year-of-netflix.jpg"
    },
    {
        "name": "Air Jordans",
        "price": 125,
        "photo": "https://neal.fun/spend/images/air-jordans.jpg"
    },
    {
        "name": "Airpods",
        "price": 199,
        "photo": "https://neal.fun/spend/images/airpods.jpg"
    },
    {
        "name": "Gaming Console",
        "price": 299,
        "photo": "https://neal.fun/spend/images/gaming-console.jpg"
    },
    {
        "name": "Drone",
        "price": 350,
        "photo": "https://neal.fun/spend/images/drone.jpg"
    },
    {
        "name": "Smartphone",
        "price": 699,
        "photo": "https://neal.fun/spend/images/smartphone.jpg"
    },
    {
        "name": "Bike",
        "price": 800,
        "photo": "https://neal.fun/spend/images/bike.jpg"
    },
    {
        "name": "Kitten",
        "price": 1500,
        "photo": "https://neal.fun/spend/images/kitten.jpg"
    },
    {
        "name": "Puppy",
        "price": 1500,
        "photo": "https://neal.fun/spend/images/puppy.jpg"
    },
    {
        "name": "Auto Rickshaw",
        "price": 2300,
        "photo": "https://neal.fun/spend/images/auto-rickshaw.jpg"
    }
    ]
      }
    }
}
</script>

<style scoped>
img {
    border-radius: 50%;
    height: 125px;
    width: 125px;
    margin: auto;
    display: block;
    margin: 10px auto 20px;
}
.section {
    max-width: 1000px;
    margin: 0 auto;
}
.board {
    font-size: 32px;
    font-weight: bold;
    text-align: center;
    padding: 30px 20px;
    margin-bottom: 10px;
    background-color: white;
}
.listItens{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
