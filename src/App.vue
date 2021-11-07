<template>
  <button @click="authenticate" class="bg-green">Login</button>
  <div id="nav">
    <router-link to="/home">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </div>
  <button @click="redirect">Redirect</button>
  <button @click="back">Go Back</button>
  <button @click="forward">Go Forward</button>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

#nav a.router-link-exact-active {
  color: #fff;
  background-color: crimson;
}
button {
  margin: 0 10px;
  padding: 10px;
  border: none;
  border-radius: 4px;
}
.bg-green {
  background: #48b883;
}
</style>

<script>
export default {
  data() {
    return {
      authenticated: false,
    };
  },
  methods: {
    redirect() {
      this.$router.push({ name: "Home" });
    },
    forward() {
      this.$router.go(+1);
    },
    back() {
      this.$router.go(-1);
    },
  },
  methods: {
    authenticate() {
      localStorage.setItem("token", "dsgjlbljbiusfbuidsbidsubsduibn");
    },
  },
};
</script>
