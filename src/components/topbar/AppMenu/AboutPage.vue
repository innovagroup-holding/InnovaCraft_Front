<template>
  <li class="nav-item dropdown">
    <router-link
      class="nav-link dropdown-toggle arrow-none d-flex justify-content-between align-items-center w-100"
      :class="menuItemActive('pages', currentRouteName) && 'active'"
      :to="{ name: 'about.v4' }"
    >
      About Us
      <!-- <font-awesome-icon :icon="faAngleDown" class="fa-sm ms-1" /> -->
    </router-link>
    <!-- <div class="dropdown-menu">
      <template v-for="(item, idx) in menuItems" :key="item.key + idx">
        <MenuItemWithChildren v-if="item.children" :item="item" />
        <MenuItem v-else :item="item" />
      </template>
      <li>
        <hr class="dropdown-divider" />
      </li>
      <li>
        <a class="dropdown-item" :href="supportLink">
          <BIconLifePreserver class="me-2" />
          Support
        </a>
      </li>
      <li>
        <a
          class="dropdown-item"
          href="https://mizzle-vue.vercel.app/docs/index.html"
          target="_blank"
        >
          <b-card-text class="me-2" />
          Documentation
        </a>
      </li>
    </div> -->
  </li>
</template>

<script lang="ts" setup>
import router from '@/router'
import { supportLink } from '@/helpers'
import type { MenuItemType } from '@/helpers/menu'
import MenuItem from '@/components/topbar/AppMenu/MenuItem.vue'
import MenuItemWithChildren from '@/components/topbar/AppMenu/MenuItemWithChildren.vue'
import { menuItemActive } from '@/components/topbar/AppMenu/getActiveClass'
import { faAngleDown } from '@fortawesome/free-solid-svg-icons'
import { BIconLifePreserver } from 'bootstrap-icons-vue'

type PagesMenuDropdownProps = {
  menuItems: MenuItemType[]
}

defineProps<PagesMenuDropdownProps>()

const currentRouteName = router.currentRoute.value.name
</script>
