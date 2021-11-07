<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>{{ job.name }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "Jobs",
  data() {
    return {
      jobs: [
        {
          name: "Software Developer",
          id: 1,
          desc: "New Job",
        },
        {
          name: "Air Force Piolot",
          id: 2,
          desc: "Prestegius Job",
        },
        {
          name: "Civil Engineer",
          id: 3,
          desc: "Government Job",
        },
      ],
    };
  },
};
</script>

<style>
.job h2 {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
