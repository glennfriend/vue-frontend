<template>
  <v-layout justify-center>

    <button
      v-for="(link, i) in importantLinks"
      :key="i"
      :href="link.href"
      type="button"
      class="subheading mx-3"
      v-on:click="reverseMessage"
      target="_blank"
    >
      {{ link.text }}/{{ message }}
    </button>

  </v-layout>
</template>

<script>
  export default {
    methods: {
      reverseMessage: function () {
        this.message = this.message.split('').reverse().join('')
      }
    },
    data: () => ({
      message: "123",
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com'
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com'
        },
      ],
      bbb: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com'
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com'
        },
      ],
    })
  }
</script>

<style>

</style>
