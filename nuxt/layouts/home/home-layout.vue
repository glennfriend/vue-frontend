<template>
  <v-app>
    <!-- top -->
    <v-toolbar app>
      <!--
      <v-btn flat to="/inspire">
        <span class="mr-2">Inspire</span>
      </v-btn>
      -->

      <v-btn flat v-for="(url, i) in routes" :key="i" :to="url.to" router exact>
        <span class="mr-2">{{ url.title }}</span>
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn flat href="#">
        <span class="mr-2">Login</span>
      </v-btn>
    </v-toolbar>
    <!-- top -->

    <!-- content -->
    <v-content>
      <v-container fluid grid-list-md>
        <nuxt/>
      </v-container>
    </v-content>
    <!-- content -->
  </v-app>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      routes: [
        {
          title: 'Home',
          to: '/'
        },
        {
          title: 'Inspire',
          to: '/inspire'
        },
        {
          title: 'Welcome',
          to: '/welcome'
        }
      ]
    }
  }
}
</script>
