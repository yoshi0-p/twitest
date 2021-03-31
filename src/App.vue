<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
var Twitter = require('twitter');
var client = new Twitter({
	consumer_key:'RZcJ9CDJ0vm0i0JXJjzJJSmXy',
	consumer_secret: 'uD83zFPIoLNzdpbyJJ3j8StjCusQNHqUIdfMR1hLqPNDcph1uh',
	access_token_key: '1352141169417850883-e7osAxtc1UUAeQPW2P3PG3CBVEiX0F',
	access_token_secret: 'ZvqjNFJV8FEiaxJEzoPOUJb94peMII3oou24N0bss8qRk'});

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
  methods:{
    xxx(){
var params = {screen_name: 'nodejs'};
client.get('statuses/user_timeline', params, function(error, tweets,) {
  if (!error) {
    console.log(tweets);
  }
});
    }
  },
  created() {
    this.xxx();
  },
};
</script>
