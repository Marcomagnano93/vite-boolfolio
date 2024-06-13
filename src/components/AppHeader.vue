<script>

export default {
  components: {
  },
  data() {
    return {
    }
  }
}

</script>

<template>
    <header>
    <div class="container-fluid py-4">
      <div class="d-flex gap-4 justify-content-center align-items-center">
          <RouterLink :to="{ name: 'home' }">Home</RouterLink>
          <RouterLink :to="{ name: 'portfolio'}">Progetti</RouterLink>
          <RouterLink :to="{ name: 'contact'}">Contattaci</RouterLink>
      </div>
    </div>

  </header>

</template>

<style></style>