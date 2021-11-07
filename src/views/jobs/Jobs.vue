<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h5>{{ job.name }}</h5>
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

<style></style>
