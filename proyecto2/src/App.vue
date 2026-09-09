<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-green-9 text-white">
      <q-toolbar>
        <q-btn
          dense
          flat
          round
          icon="menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title
          style="display: flex; align-items: center; gap: 12px;"
        >
          <q-avatar>
            <img alt="sena logo" src="../src/assets/logos/sena-logo.png">
          </q-avatar>
          <span>Centro Agroturístico - SENA</span>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      :mini="miniState"
      @mouseenter="miniState = false"
      @mouseleave="miniState = true"
      mini-to-overlay
      :width="220"
      :breakpoint="500"
      bordered
      class="bg-grey-2"
    >
      <q-scroll-area class="fit" :horizontal-thumb-style="{ opacity: 0 }">
        <q-list padding role="none">
          <q-item
            clickable
            v-ripple
            to="/Enfermeria"
            aria-label="Enfermería"
          >
            <q-item-section avatar>
              <q-icon name="medical_services" color="green-9" />
            </q-item-section>
            <q-item-section>Enfermería</q-item-section>
          </q-item>

          <q-item
            clickable
            v-ripple
            to="/Bienestar"
            aria-label="Bienestar"
          >
            <q-item-section avatar>
              <q-icon name="favorite" color="green-9" />
            </q-item-section>
            <q-item-section>Bienestar</q-item-section>
          </q-item>

          <q-item
            clickable
            v-ripple
            to="/Cafeteria"
            aria-label="Cafetería"
          >
            <q-item-section avatar>
              <q-icon name="restaurant" color="green-9" />
            </q-item-section>
            <q-item-section>Cafetería</q-item-section>
          </q-item>

          <q-item
            clickable
            v-ripple
            to="/Coordinacion"
            aria-label="Coordinación"
          >
            <q-item-section avatar>
              <q-icon name="admin_panel_settings" color="green-9" />
            </q-item-section>
            <q-item-section>Coordinación</q-item-section>
          </q-item>

          <q-item
            clickable
            v-ripple
            to="/Biblioteca"
            aria-label="Biblioteca"
          >
            <q-item-section avatar>
              <q-icon name="book" color="green-9" />
            </q-item-section>
            <q-item-section>Biblioteca</q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title style="display:flex; align-items:center; gap:8px;">
          <q-avatar>
            <img alt="Quasar logo" src="/logo/logo-mono-white.svg">
          </q-avatar>
          <div>Centro Agroturístico - SENA</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const leftDrawerOpen = ref(false)
const miniState = ref(true)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>