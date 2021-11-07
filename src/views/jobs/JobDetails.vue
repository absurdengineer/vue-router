<template>
  <h1>Job Details</h1>
  <p>The Job id is {{ id }}</p>
</template>

<script>
export default {
  name: "JobDetails",
  props: ["id"],
  data() {
    return {
      id: this.id,
    };
  },
};
</script>

<style></style>
