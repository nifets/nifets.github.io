<template>
  <q-layout view="lHh Lpr lFf" class="q-ml-xl">
    <h3>nifets.dev</h3>

    <q-list>
      <EssentialLink
        v-for="link in essentialLinks"
        :key="link.title"
        v-bind="link"
      />
    </q-list>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import EssentialLink, {
  EssentialLinkProps,
} from 'components/EssentialLink.vue';
const essentialLinks: EssentialLinkProps[] = [
  {
    title: 'Torus Align',
    caption: 'align.nifets.dev',
    link: 'https://align.nifets.dev',
  },
  {
    title: 'Depths',
    caption: 'depths.nifets.dev',
    link: 'https://depths.nifets.dev',
  },
  {
    title: 'Github',
    caption: 'github.com/nifets',
    link: 'https://github.com/nifets',
  },
  {
    title: 'Youtube',
    caption: 'youtube.com/channel/nifets',
    link: 'https://www.youtube.com/channel/UCgPyEh1PPO5bNcGXpjaEhLg',
  },
];
</script>
