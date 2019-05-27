<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>COM3</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color="info" raised @click="connect">Connect</v-btn>
      <v-btn flat href="https://github.com/kamiyaowl/com3" target="_blank">
        <span class="mr-2">Github</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <!-- <HelloWorld/> -->
    </v-content>
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld'

export default {
  name: "App",
  components: {
    //HelloWorld
  },
  data() {
    return {
      isConnected: false,
    };
  },
  methods: {
    connect: async function() {
      const device = await navigator.usb.requestDevice({'filters': []})
    },
    disconnect: function() {
      
    },
  }
};
</script>
