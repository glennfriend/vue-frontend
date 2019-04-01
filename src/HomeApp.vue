<template>
  <v-app>

    <!-- top -->
    <v-toolbar app >

      <v-btn flat href="#" >
        <span class="mr-2">Welcome</span>
      </v-btn>
      <v-spacer></v-spacer>

      <v-btn flat href="#" >
        <span class="mr-2">Login</span>
      </v-btn>

    </v-toolbar>
    <!-- top -->

    <!-- content -->
    <v-content>
      <v-container fluid grid-list-md>
        <v-layout row>

          <v-flex grow pa-1>
            <v-card color="darken-3">

              <!--
              <v-card-text>
                #text<br>
              </v-card-text>
              -->

              <v-card-text>
                <MyButton />
              </v-card-text>

            </v-card>
          </v-flex>

        </v-layout>
      </v-container>
    </v-content>
    <!-- content -->

  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MyButton from './components/MyButton.vue'

export default {
  name: 'HomeApp',
  components: {
    //HelloWorld,
    MyButton,
  },
  data () {
    return {
    }
  }
}
</script>
