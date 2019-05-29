<template>
  <v-app 
   
  >


    <v-navigation-drawer
      width="100%"
      class="overlay"
      v-model="drawer"
      fixed
      app
      v-if="$vuetify.breakpoint.smAndDown"
    >
      <ul>
          <li v-for="item in items">
              {{ item.title }}
          </li>
      </ul>
    </v-navigation-drawer>


    <v-toolbar
      fixed
      app
      :class=" scrollTop == 0 ? 'camouflage raise' : 'raise' "
      :flat="scrollTop == 0 "
    >
     
     
      <v-toolbar-title v-text="title" />
      <v-spacer />

      <v-btn
        icon
        size="36px"
        v-if="$vuetify.breakpoint.smAndDown"
        @click.stop="drawer = true"
      >
        <v-icon>menu</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content id="main-body" v-scroll:#main-body="scrolledBody">
     <div  v-scroll:#main-body="scrolledBody">
        <nuxt />
      </div>
    </v-content>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-tile @click.native="right = !right">
          <v-list-tile-action>
            <v-icon light>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
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
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },

  computed: {

     scrollTop(){
          return this.offsetTop
     }
  },


  methods: {

      scrolledBody(e){
            alert(e.target.scrollTop)
           this.offsetTop = e.target.scrollTop
           
      }
  }
}
</script>
<style>
.camouflage {

    background-color: rgba(186,196,209,.31373) !important;
}

.overlay {
    opacity: 0.5;
    background-color: black;
}

ul {
   display: flex;
   flex-direction: column;
   list-style: none;
   margin: auto;
}

li {
     font-weight: 500;
     text-transform: capitalize;
     color: black;
}

.raise {
    z-index: 10000;
    display: block;
    background-color: #fff;
}

</style>