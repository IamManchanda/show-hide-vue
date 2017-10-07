<template>
  <div class="grid-container">
    <div class="grid-x grid-margin-x grid-padding-y">
      <div class="cell margin-top-2">
        <button class="button small alert"
                @click="selectedComponent = 'AppRed'">Show Red Callout</button>
        <button class="button small success"
                @click="selectedComponent = 'AppGreen'">Show Green Callout</button>
        <button class="button small primary"
                @click="selectedComponent = 'AppBlue'">Show Blue Callout</button>
        <keep-alive>
          <component :is="selectedComponent"></component>
        </keep-alive>
      </div>
    </div>
  </div>
</template>

<script>
import AppRed from './components/AppRed.vue';
import AppGreen from './components/AppGreen.vue';
import AppBlue from './components/AppBlue.vue';

export default {
  data() {
    return {
      selectedComponent: 'AppRed'
    };
  },
  components: { AppRed, AppGreen, AppBlue }
}
</script>

<style lang="scss">

</style>
