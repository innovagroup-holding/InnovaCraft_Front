<template>
  <StickyHeader class-name="header-absolute">
    <nav class="navbar navbar-expand-xl navbar-nav dropdown-hover">
      <b-container>
        <LogoBox class-name="me-0" />

        <AppMenu ulClass="mx-auto" showContactUs showDocs />

        <ul class="nav align-items-center dropdown-hover ms-sm-2">
          <ThemeToggleDropdown />

          <li class="nav-item d-none d-sm-block">
            <router-link class="btn btn-sm btn-primary mb-0" :to="{ name: 'contact.v1' }">
              Hire us
            </router-link>
          </li>

          <li class="nav-item">
            <MobileNavbarToggler />
          </li>
        </ul>
      </b-container>
    </nav>
  </StickyHeader>
</template>

<script lang="ts" setup>
import { BIconPersonCircle } from 'bootstrap-icons-vue'
import StickyHeader from '@/components/topbar/StickyHeader.vue'
import LogoBox from '@/components/topbar/LogoBox.vue'
import ThemeToggleDropdown from '@/components/topbar/ThemeToggleDropdown.vue'
import MobileNavbarToggler from '@/components/topbar/MobileNavbarToggler.vue'
import AppMenu from '@/components/topbar/AppMenu/index.vue'
import { buyLink } from '@/helpers'
</script>
