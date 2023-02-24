<script lang="ts" setup>
// ❗ issue also encounters if you import file that has import
// import { config } from '../themeConfig';
// console.log('config :>> ', config);

import { h } from 'vue';
import { VThemeProvider } from 'vuetify/components';

const wrapper = h(VThemeProvider, { theme: 'dark' })
</script>

<template>
  <v-app>
    <v-main>
      <RouterView></RouterView>
      <component :is="wrapper">
        <VBtn>Button</VBtn>
      </component>
    </v-main>
  </v-app>
</template>
