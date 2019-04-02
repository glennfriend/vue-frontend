<template>
  <v-container fluid>
    <v-layout justify-space-around class="mb-2">
      <span class="group pa-2">
        <v-icon>home</v-icon>
        <v-icon medium>home</v-icon>
        <v-icon large>home</v-icon>
        <v-icon x-large>home</v-icon>
      </span>

      <span class="group pa-2 teal">
        <v-icon dark>home</v-icon>
        <v-icon dark medium>home</v-icon>
        <v-icon dark large>home</v-icon>
        <v-icon dark x-large>home</v-icon>
      </span>

      <span class="group pa-2">
        <a
          href="https://material.io/tools/icons/?style=baseline"
          target="_blank"
        >Google Material Icons</a>
      </span>
    </v-layout>

    <v-btn flat v-for="(name, i) in icons" :key="i">
      <div>
        {{ name }}
        <v-icon large>{{ name }}</v-icon>
      </div>
    </v-btn>
  </v-container>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      icons: ['home', 'event', 'info']
    }
  }
}
</script>
