<template>
  <div class="grid-container">
    <div class="grid-x grid-margin-x grid-padding-y">
      <div class="cell margin-top-2">
        <button class="button small margin-right-1 alert"
                @click="selectedComponent = 'AppRed'">Load Red Template</button>
        <button class="button small margin-right-1 success"
                @click="selectedComponent = 'AppGreen'">Load Green Template</button>
        <button class="button small margin-right-1 primary"
                @click="selectedComponent = 'AppBlue'">Load Blue Template</button>
        <div><br /></div>
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
