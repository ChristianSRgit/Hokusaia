<template>
  <v-app>
    <v-content>
      <Header/>
    </v-content>
    <v-content>
      <Meal/>
    </v-content>
    <v-content>
      <Footer/>
    </v-content>
  </v-app>
</template>

<script>
import Meal from './components/Meal';
import Header from './components/Header';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Meal,
    Header,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
