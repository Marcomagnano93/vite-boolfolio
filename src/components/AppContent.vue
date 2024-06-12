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
          <ul class="row gap-3">
            <li class="card" v-for="project in projects">
                <div class="card-header">
                    {{ project.title }}
                </div>
                <div class="card-body">
                  <p>
                    {{ project.description }}
                  </p>
                  <p>
                    <a :href="project.git">Git Link</a>
                  </p>
                    
                </div>
            </li> 
          </ul>
        </div>
    </section>
  </main>

</template>

<style></style>