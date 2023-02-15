<template>
  <div class="navbar">
    <h1>My VueX App Todos</h1>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li v-if="auth.isAuthenticated">
        Total Todos: {{ todos.length }}
        <button @click="TOGGLE_AUTH">Logout</button>
      </li>
      <button v-else @click="TOGGLE_AUTH">Login</button>
    </ul>
  </div>
</template>

<script>
import { mapMutations, mapState } from "vuex";
export default {
  name: "NavBar",

  data() {
    return {};
  },
  computed: mapState(["todos", "auth"]),
  mounted() {},

  methods: mapMutations(["TOGGLE_AUTH"]),
};
</script>

<style >
.navbar {
  padding: 5px;
  text-align: center;
  background: rgb(240, 240, 240);
  color: black;
}

.navbar ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  list-style: none;
  padding: 0;
}
</style>