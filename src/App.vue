<template>
<div class="background">
 <Header />

 <div>
  <router-view/>


 </div>
 </div>
</template>

<script>
import Header from '@/components/Header'
export default {
  components:{
    Header,
  },
}

</script>
<style>
.background{
  background-color: #14161a;
  min-height: 100vh;
}
</style>
