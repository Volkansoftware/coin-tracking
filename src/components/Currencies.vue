<template>
<div v-for="(currency) in currencies" :key="currency.id" class="coin-container text-white">
  <div class="coin-row">
    <div class="coin">
      <img :src="currency.image" alt="crypto">
      <h1>{{currency.name}}</h1>
      <p class="coin-symbol">{{currency.symbol}}</p>
    </div>
    <div class="coin-data">
      <p class="coin-price">${{currency.current_price}}</p>
      <p class="coin-volume">${{currency.total_volume}}</p>
    </div>
            <p className='coin-percent red' v-if="currency.price_change_percentage_1h_in_currency<0"> {{currency.price_change_percentage_1h_in_currency.toFixed(2)}}%</p>
            <p className='coin-percent green' v-else>{{currency.price_change_percentage_1h_in_currency.toFixed(2)}}%</p>
          
  </div>
</div>

</template>

<script>

export default {
    name:['Currencies'],
    props:['currencies']
}

</script>
<style>

.coin-container {
  display: flex;
  justify-content: center;
}

.coin-row {
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: center;
  height: 80px;
  border-bottom: 1px solid #d7d7d7;
  width: 900px;
}

.coin {
  display: flex;
  align-items: center;
  padding-right: 24px;

  min-width: 300px;
}

.coin h1 {
  font-size: 16px;
  width: 150px;
}

.coin img {
  height: 30px;
  width: 30px;
  margin-right: 10px;
}

.coin-symbol {
  text-transform: uppercase;
}

.coin-data {
  display: flex;
  text-align: right;
  justify-content: space-between;
  width: 100%;
}

.coin-price {
  width: 110px;
}

.coin-volume {
  width: 155px;
}

.coin-marketcap {
  width: 230px;
}

.coin-percent {
  width: 100px;
  margin-left: 10px;
}

.red {
  color: #f00606;
}

.green {
  color: #11d811;
}


</style>
