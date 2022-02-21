  <template>
   <div class="banner">
     <div class="bannerContent">
       <div class="tagline">
        <h2 class="typography">Coin Tracker </h2>
        <p class="subtitle2">Kripto ile ilgili tüm bilgileri  Coin Tracker'dan edinin ! </p>
       </div>
     </div>
  </div>

</template>
 
<script>

export default {
  name: 'Banner'
}
</script>
 <style>
 .banner{
   background-image: url('https://raw.githubusercontent.com/piyush-eon/react-crypto-tracker/master/public/banner2.jpg');
 }
.bannerContent{
  height: 400px;
  display: flex;
  flex-direction: column;
  padding-top: 25px;
  
}
.tagline{
display: flex;
height: 80%;
justify-content: center;
flex-direction: column;
text-align: center;
}
.typography{
font-weight: bold;
margin-bottom: 15px;
color: white;
font-size: 8vh;
}
.subtitle2{
  color: darkgray;
  
}
 </style>
