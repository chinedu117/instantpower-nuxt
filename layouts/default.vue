<template>
  <v-app 

  >
    <div
      class="overlay"
      v-if="$vuetify.breakpoint.smAndDown && drawer"
    >
      <div style="width: 100%; display:flex; padding: 5px 5px 0  0;"><v-icon  size="72px"  color="white" @click="drawer = false">close</v-icon></div>
      <ul>
          <li v-for="(item,index) in items"
           :key="index"
          >
              {{ item.title }}
          </li>
      </ul>
    </div>


    <v-toolbar
      fixed
      app
      :class=" scrollTop == 0 ? 'camouflage ' : 'raise' "
      :flat="scrollTop == 0 "
    >
      <logo/>
      
      <v-spacer />
       
       <v-toolbar-items v-if="$vuetify.breakpoint.mdAndUp">

           <v-btn class="main_link" flat v-for="(item,index) in items"
           :key="index">
              {{ item.title }}
          </v-btn>

       </v-toolbar-items>
      <v-btn
        icon
        size="36px"
        v-if="$vuetify.breakpoint.smAndDown"
        @click.stop="drawer = true"
      >
        <v-icon>menu</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content id="main-body" v-scroll="scrolledBody">
     <div  >
        <nuxt  />
      </div>
    </v-content>
    
    <v-footer
      app
      class="footer"
    >
      <span>©2019 InstantPower, DataPlus Interactive, all rights reserved.</span>
    </v-footer>
  </v-app>
</template>

<script>
import Logo from '~/components/Logo.vue'
export default {
  data() {
    return {
      offsetTop: 0,
      scrolled: false,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'apps',
          title: 'Retrieve Token',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'FAQ',
          to: '/inspire'
        },
        {
          icon: 'bubble_chart',
          title: 'Contact Us',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  
  components: { Logo },

  computed: {

     scrollTop(){
          return this.offsetTop
     }
  },


  methods: {

      scrolledBody(){
           
         
           this.offsetTop = document.documentElement.scrollTop
           
      }
  }
}
</script>
<style>

h1, h2, h3, h4, h5, h6 {
    color: #615f8e !important;
}
.camouflage {

    background-color: rgba(186,196,209,.31373) !important;
}

.overlay {
    background-color: rgba(0,0,0,.956);
    position: fixed;
    top: 0;
    left: 0;
    width:100%;
    height: 100vh;
    z-index: 10000000;
    color: white;
}

ul {
   display: flex;
   list-style: none;
   flex-direction: column;
   align-items: center;
   justify-content: center;
   margin: auto;
   width: 100%;
   height: 70vh;
}

li {
     font-weight: 700;
     text-transform: capitalize;
     opacity: 1 !important;
     padding: 10px;
     color: #615f8e;
}

.raise {
    z-index: 10000;
    display: block;
    background-color: #fff;
    border-bottom: 2px solid #615f8e !important;
}

.main_link {
   color: #615f8e !important;
   font-weight: 700;
   font-size: 24px;
   
}

.main_link:hover {
    color: red !important;

}

.footer {
   background-color: black
   color: white;
   padding: 100px 0;
   margin: 0 auto;
}

</style>