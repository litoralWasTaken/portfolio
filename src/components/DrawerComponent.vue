<template>
  <div class="drawer-main-container">
    <div class="drawer-title-row">
      {{ title }}

      <FontAwesomeIcon @click="isExtended = !isExtended" :icon="`fa-solid ${chevronClass}`" class="drawer-chevron">
      </FontAwesomeIcon>
    </div>

    <div v-if="isExtended" class="drawer-content">
      <ul>
        <li v-for="(line, index) in content" v-bind:key="index"> {{ line }}</li>
      </ul>
    </div>

  </div>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {

  watch: {
    isExtended(newVal) {
      this.chevronClass = newVal ? 'fa-chevron-up' : 'fa-chevron-down'
      console.log(this.chevronClass);

    }
  },
  components: {
    FontAwesomeIcon
  },

  props: {
    title: {
      type: String,
      required: true
    },
    content: {
      type: Array,
      required: true
    }
  },

  data() {
    return {
      isExtended: false,
      chevronClass: 'fa-chevron-down'
    }
  },

}
</script>
<style scoped>
.drawer-main-container {
  border: 2px solid var(--secondary);
  padding: 5px;
  margin: 5px 5px 0px 5px;
  border-radius: 4px;
}

.drawer-chevron {
  height: 25px;
  width: 25px;
}

.drawer-title-row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
