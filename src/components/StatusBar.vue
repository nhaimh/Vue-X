<template>
  <div class="status-bar" v-if="auth.isAuthenticated">
    <p>Done</p>
    <ul>
      <li v-for="todo in doneTodos" :key="todo.id">
        {{ todo.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import { mapGetters, mapState } from "vuex";
// import { mapState } from "vuex";
export default {
  name: "StatusBar",

  data() {
    return {};
  },
  computed: { ...mapGetters(["doneTodos"]), ...mapState(["auth"]) },

  mounted() {},

  methods: {},
};
</script>

<style >
.status-bar {
  padding: 5px;
  text-align: center;
  background: rgb(240, 240, 240);
  color: black;
}
</style>