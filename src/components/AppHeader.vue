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
    <div class="container-fluid">
      <div class="d-flex">
          <RouterLink :to="{ name: 'home' }">Home</RouterLink>
          <RouterLink :to="{ name: 'portfolio'}">Progetti</RouterLink>
          <RouterLink :to="{ name: 'contact'}">Contataci</RouterLink>
      </div>
    </div>

  </header>

</template>

<style></style>