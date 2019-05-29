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
                <v-select outline placeholder="Select your State" :items="states" ></v-select> 
               </v-flex>
            </v-layout>
          
          
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
                   <v-btn width="100%" outline class="mx-0 my-3">Buy Electricity Now<v-icon>chevron_right</v-icon></v-btn>
               </v-flex>
            </v-layout>
          
           </v-container>
        </v-card>
     </v-flex>
   </v-layout>
   </v-container>
</section>


   
     <v-container> 
      <section class="second-band"> 
       <!-- <v-layout row class="justify-end" align="end">
          <v-flex xs12 md5 > -->
            
              <h2 class="display-3  font-weight-bold pt-2" style="flex:0.4">The most convenient way <br>to buy power</h2>

          <!-- </v-flex>
       </v-layout> -->
        </section>
      </v-container>

  
   

 
  
  
</div>

 
</template>

<script>
export default {

  data(){
     return {
         offsetTop: 0,
        states: [ 'Nassarawa','Kogi','Abuja','Edo'],
     }
  },

  computed: {
      
  },

  methods: {

       
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

.second-band {
   background-color: #fff;
   min-height: 60vh !important;
   display: flex !important;
   flex-direction: row;
   justify-content: flex-end;
   align-items: flex-end;
   width: 100%;
}

.landing-page-background {
   background-color: rgba(186,196,209,.31373) !important;
   z-index: 2 !important;
   height: 70vh;
   position: relative;
}

}

.landing-page-background {
   background-color: rgba(186,196,209,.31373) !important;
   z-index: 0 !important;
   height: 70vh;
   position: relative;
}


.second-band {
   display: block;
   min-height: 90vh;
}


</style>