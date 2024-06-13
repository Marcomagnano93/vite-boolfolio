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
    <div class="container-fluid py-4 mb-3 header-bg">
      <div class="d-flex gap-4 justify-content-center align-items-center">

          <RouterLink :class="$route.fullPath === '/' ? 'btn btn-warning' : 'btn btn-info'"  :to="{ name: 'home' }">Home</RouterLink>
          <RouterLink :class="$route.fullPath === '/portfolio' ? 'btn btn-warning' : 'btn btn-info'"  :to="{ name: 'portfolio'}">Progetti</RouterLink>
          <RouterLink :class="$route.fullPath === '/contact' ? 'btn btn-warning' : 'btn btn-info'"  :to="{ name: 'contact'}">Contattaci</RouterLink>
      </div>
    </div>

  </header>

</template>

<style>
.header-bg{
  background-color: rgb(33, 33, 81);
}
</style>