<template>
  <div class="text-center">
    <p class="text-muted">Powered by</p>
    <ul class="list-inline">
      <li class="list-inline-item mx-2" v-for="(icon, idx) in icons" :key="idx">
        <a :href="icon.href" target="_blank" :title="icon.href">
          <font-awesome-icon :icon="icon.classes" class="fa-lg" :style="{'color': icon.color}" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

export default {
  name: 'PoweredByFoot',
  components: {
    FontAwesomeIcon
  },
  props: {
    icons: {
      required: true,
      type: Array
    }
  }
}
</script>
