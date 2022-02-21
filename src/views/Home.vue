  <template>
   <Banner/>
<Currencies :currencies="currencies"/>

</template>
 
<script>
import Banner from '@/components/Banner'
import Vue from 'vue';
import  axios from 'axios'
import VueAxios from 'vue-axios'
import Currencies from '@/components/Currencies'

export default {
  name: 'Home',
  data()
  {
    return{
    url:'https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=10&page=1&sparkline=false&price_change_percentage=1h',
    currencies:[]
  };
  },
  mounted()
  {
    axios.get(this.url).then(response => (this.currencies=response.data));
  },
  components:{
    Currencies,
    Banner,
  },
 
}
</script>
 <style>
 
 </style>
