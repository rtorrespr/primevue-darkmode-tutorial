<template>
  <main>
    <div class="main">
      <Button label="Aplicar dark mode" @click="toggle" />
    </div>
  </main>
</template>

<script>
import Button from 'primevue/button';

export default {
  data: () => ({
    isDarkMode  : false,
  }),
  methods: {
    toggle() {
      if( this.isDarkMode )
        document.documentElement.classList.remove('darkMode');
      else
        document.documentElement.classList.add('darkMode');

      this.isDarkMode = !this.isDarkMode;
    }
  },
  components: {
    Button
  }
}
</script>

<style scoped>
.main {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
}
</style>