<template>
    <div class="card">
        <img  class="img-card" :src="photo" alt="image item">
        <p class="name-card">{{name}}</p>
        <span class="price-card">${{price}}</span>
        <div class="group">
            <button class="button sell" @click="sell(item)">Sell</button>
            <input  min="0" class="input-card" v-model="value" type="number" />
            <button class="button buy" @click="buy(item)">Buy</button>
        </div>
    </div>
</template>


<script>

export default {
    name: "Card",
    data(){
        return {value: 0,
        }
    },
    props: ['name','photo', 'price'],
    methods: {
        sell(item){
            if(this.value > 0) {
                this.$emit('sell-change', item)
                this.value--
            }
            
        },
        buy(item){
            this.$emit('buy-change', item)
            this.value++
        },
    },
}
</script>

<style scoped>
.card {
    box-sizing: border-box;
    padding: 20px 15px;
    max-width: 323px;
    background-color: white;
    margin: 0 10px 10px 0
}
.img-card {
    display: block;
    margin: 0 auto;
    padding: 15px 0px;
    height: 120px;
    max-width: 100%;
    object-fit: contain;
    user-select: none;
}
.button {
    font-size: 16px;
    cursor: pointer;
    padding: 10px 12px;
    border-radius: 3px;
    text-align: center;
    color: white;
    border: medium none;
    font-weight: bold;
    user-select: none;
    flex-grow: 1;
    flex-shrink: 1;
    width: 25%;
}
.buy {
    background: rgba(0, 0, 0, 0) linear-gradient(rgb(46, 204, 113), rgb(26, 188, 156)) repeat scroll 0% 0%;
}
.sell {
    background: rgba(0, 0, 0, 0) linear-gradient(rgb(245, 59, 130), rgb(245, 59, 87)) repeat scroll 0% 0%;
}
.group {
    display: flex;
}
.input-card {
    font-size: 16px;
    padding: 9px 12px;
    border-radius: 3px;
    border: 1px solid rgb(178, 190, 195);
    color: rgb(51, 51, 51);
    text-align: center;
    flex-grow: 1;
    flex-shrink: 1;
    width: 25%;
}
.name-card {
    font-size: 22px;
    font-weight: bold;
    margin: 0;
}
.price-card {
    font-size: 20px;
    color: rgb(36, 196, 134);
}
</style>