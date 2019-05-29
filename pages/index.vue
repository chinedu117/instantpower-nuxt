<template>
<div>
 <section class="landing-page-background">
    <v-container class="justify-content-start">

     <div class="image-box">
        
     </div>
     <v-layout class="mt-2">
        <v-flex xs12 md6>
            <h1 class="display-3 font-weight-bold">Reliable, Convenient, Electricity for all.</h1>   
        </v-flex>
     </v-layout>



     <v-layout row fluid>
      <v-flex xs12 md8>

        <v-card class="elevate-2 card_custom">

          <v-container>

            
          
            <v-layout wrap class="my-2"><v-flex xs12><h2 class="display-1 "> Buy Electricity in 60 Seconds </h2> </v-flex></v-layout>
          
          
            <v-layout>
              <v-flex xs12>
                <v-text-field outline placeholder="Your Meter Number here"></v-text-field> 
               </v-flex>
            </v-layout>
          
          
            <v-layout>
              <v-flex xs12>
               <v-text-field outline placeholder="Amount in Naira"></v-text-field> 
            </v-flex>
            </v-layout>
          
          
            <v-layout>
              <v-flex xs12>
                <v-text-field outline placeholder="Your Phone Number"></v-text-field>
            </v-flex>
            </v-layout>
          
          
            <v-layout>
              <v-flex xs12>
                <v-text-field outline placeholder="Your Meter Number here"></v-text-field> 
            </v-flex>
            </v-layout>
          
          
            <v-layout>
              <v-flex xs12>
                <v-text-field outline placeholder="Email Address"></v-text-field>
            </v-flex>
            </v-layout>
          
          
            <v-layout>
              <v-flex xs12>
                   <v-btn width="100%"  outline class="mx-0 my-3">Buy Electricity Now<v-icon>user</v-icon></v-btn>
               </v-flex>
            </v-layout>
          
           </v-container>
        </v-card>
     </v-flex>
   </v-layout>
   </v-container>
</section>


   <section class="second-band"> 
     <v-container> 
       <v-layout  wrap class="justify-end" >
          <v-flex xs12 md4 >
            
              <h2 class="display-3  font-weight-bold pt-2">The most convenient way to buy power</h2>

          </v-flex>
       </v-layout>
      </v-container>

   </section>
   

 
  
  
</div>

 
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
<style>
.card_custom {
   border-radius: 7px;

}


 .image-box {
   display: hidden;

}

@media screen and (min-width: 900px){
   .card_custom {
      width: 600px;

  }

  .image-box{
   display: block;
   padding: 0;
   width: 300px;
   height: 300px;
   position: absolute;
   left: 50%;
   bottom: 0px;
   background-color: grey;

}

}

.landing-page-background {
   background-color: rgba(186,196,209,.31373) !important;
   z-index: 2;
   height: 70vh;
   position: relative;
}



.second-band {
   background-color: #fff;
   min-height: 60vh;
}


</style>