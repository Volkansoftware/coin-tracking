<template>
<span>

<p class="p-margin" v-for="(currency) in currencies" :key="currency.id">{{currency.name}} 

Bitcoin fiyatı anlık ${{currency.current_price}} ve 
24 saatlik işlem hacmi ${{currency.total_volume}}. Fiyat son 24 saatte {{currency.price_change_percentage_1h_in_currency.toFixed(2)}}% artmıştır.  Dolaşımda 19 Milyon 
BTC coin arzı, toplamda 21 Milyon coin arzı bulunmaktadır.FTX, şu anda bunun ticaretinin yapıldığı en aktif piyasadır.


</p>

</span>
</template>

<script>

export default {
    name:['Btc'],
    props:['currencies'],
 
}

</script>
<style>
.p-margin{
    margin: 10px;
    font-size: ;
}

</style>
