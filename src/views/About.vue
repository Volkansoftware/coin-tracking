<template>
  <div >
    <div class="container text-white">
    <h1 class="titleBtc">Bitcoin</h1>
    <h2 class="titleDesc">BTC Fiyatı ve Piyasa Verileri</h2>
    <Btc :currencies="currencies"/>
    <h2 class="titleDesc">En yüksek BTC fiyatı neydi ?</h2>
    <p class="p-margin">Bitcoin tüm zamanların en yüksek seviyesi $69.044,77  10 kasım 2021'de (3 ay önce) ulaştı. </p>
    <h2 class="titleDesc">En düşük BTC fiyatı neydi ?</h2>
    <p class="p-margin">Bitcoin tüm zamanların en yüksek seviyesi $67,81  6 temmuz 2013'te (9 yıl önce) ulaştı. </p>
    <h2 class="titleDesc">Bitcoin'i nereden alabilirim ?</h2>
    <p class="p-margin">Bitcoin'i FTX,FTX.US, Binance ve Paribudan alabilirsiniz.</p>
  </div>
  </div>
</template>

<script>
import Btc from '@/components/Btc'
import  axios from 'axios'
import VueAxios from 'vue-axios'
export default {
  name: 'About',
  data()
  {
    return{
    url:'https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=1&page=1&sparkline=false&price_change_percentage=1h',
    currencies:[]
  };
  },
  mounted()
  {
    axios.get(this.url).then(response => (this.currencies=response.data));
  },
  components:{
  Btc
  },
 
}
</script>


<style>
.titleBtc{
  margin-top: 1vh;
  color: gold !important;
  font-weight: bold;
 display: flex;
 justify-content: center;
 font-size: 4vw;
}
.titleDesc{
  margin-top: 4vh;
  font-size: 2vw;
  color: rgb(214, 219, 174);
}

</style>
