<template>
  <v-app>

    <!-- top -->
    <v-toolbar app >
      <v-toolbar-title class="headline text-uppercase">
        <span>Vue</span>
        <v-btn flat href="#" >
          <span class="mr-2">Dashboard</span>
        </v-btn>
      </v-toolbar-title>
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


          <v-flex shrink pa-1>
            <v-card dark color="green darken-1">

                <v-navigation-drawer permanent>
                  <v-toolbar flat>
                    <v-list>
                      <v-list-tile>
                        <v-list-tile-title class="title">Dashboard</v-list-tile-title>
                      </v-list-tile>
                    </v-list>
                  </v-toolbar>
                  <v-divider></v-divider>
                  <v-list dense class="pt-0">
                    <v-list-tile
                      v-for="item in items"
                      :key="item.title"
                      @click=""
                    >
                      <v-list-tile-action>
                        <v-icon>{{ item.icon }}</v-icon>
                      </v-list-tile-action>

                      <v-list-tile-content>
                        <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                      </v-list-tile-content>
                    </v-list-tile>
                  </v-list>
                </v-navigation-drawer>

            </v-card>
          </v-flex>


          <v-flex grow pa-1>
            <v-alert v-model="isShowAlert" dismissible type="success">
              This is a success alert that is closable.
            </v-alert>
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
//import Vuetify from 'vuetify'
import HelloWorld from './components/HelloWorld.vue'
import MyButton from './components/MyButton.vue'

export default {
  name: 'AdminApp',
  components: {
    //Vuetify,
    //HelloWorld,
    MyButton,
  },
  data () {
    return {
      items: [
        { title: 'Home',  icon: 'dashboard' },
        { title: 'About', icon: 'question_answer' }
      ],
      isShowAlert: true
    }
  }
}
</script>
