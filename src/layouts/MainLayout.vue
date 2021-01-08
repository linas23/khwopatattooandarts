<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated reveal>
      <q-toolbar>
        <q-toolbar-title>
          Khwopa Tattoo Inn And Art
        </q-toolbar-title>
 <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="rightDrawerOpen = !rightDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="rightDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
      side="right"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="(link,index) in essentialLinks"
          :key="index"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'About us',
    caption: '',
    icon: 'school',
    link: '/aboutUs'
  },
  {
    title: 'Shop',
    caption: '',
    icon: 'school',
    link: '/shop'
  },
    {
    title: 'Tattoo',
    caption: '',
    icon: 'school',
    link: '/tattoo'
  },
  {
    title: 'Portrait',
    caption: '',
    icon: 'school',
    link: '/portraits'
  },
  {
    title: 'Tattoo',
    caption: '',
    icon: 'school',
    link: '/tattoo'
  },
  {
    title: 'Wall art',
    caption: '',
    icon: 'school',
    link: '/wall art'
  },
  {
    title: 'Wood carvings',
    caption: '',
    icon: 'school',
    link: '/wood carvings'
  },
  {
    title: 'Painting',
    caption: '',
    icon: 'school',
    link: '/painting'
  },
];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      rightDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
