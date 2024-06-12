<script>
import axios from 'axios'

export default {
  data() {
    return {
      projects: []
    }
  },
  methods: {
    fetchData() {

      axios.get('http://127.0.0.1:8000/api/projects',{
        params: {

        }
      })
      .then((res) => {
        console.log(res.data.projects)
        this.projects = res.data.projects
      })
    }
  },
  created() {
    this.fetchData()
  },
}

</script>

<template>

  <main>
    <section class="h-100">
        <div class="container">
          <h2>Progetti:</h2>
          <ul class="row">
            <li class="col-4 card" v-for="project in projects">
                prova
            </li> 
          </ul>
        </div>
    </section>
  </main>

</template>

<style></style>