<script>
import axios from 'axios';


export default {
  data() {
    return {
      projects: []
    }
  },
  methods: {
    fetchData() {

      axios.get('http://127.0.0.1:8000/api/projects')
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
                    <p>
                        
                    </p>
                </div>
            </li>
        </ul>
</template>

<style></style>