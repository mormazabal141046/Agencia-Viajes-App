<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          Agencia de Viajes
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Menú Agencia
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
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
    title: 'Ejecutivo',
    caption: 'Módulo',
    icon: 'support_agent',
    link: '/ficha-contrato'
  },
  // {
  //   title: 'Pagos',
  //   caption: 'Portal',
  //   icon: 'payment',
  //   link: '/pagos'
  // },
  // {
  //   title: 'Reportes',
  //   caption: 'Encuentra los avances',
  //   icon: 'receipt_long',
  //   link: '/reportes'
  // },
  {
    title: 'Alumno',
    caption: 'Ficha',
    icon: 'perm_identity',
    link: '/alumno'
  },
]

export default {
  name: 'MainLayout',
  components: {
    EssentialLink
  },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
