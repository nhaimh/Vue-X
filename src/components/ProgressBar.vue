<template>
  <div v-if="auth.isAuthenticated">
    <p class="progress-bar">Progress:{{ progress }} %</p>
  </div>
</template>

<script>
import { mapGetters, mapState } from "vuex";
export default {
  name: "ProgressBar",
  computed: { ...mapGetters(["progress"]), ...mapState(["auth"]) },
  data() {
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style >
.progress-bar {
  padding: 5px;
  text-align: center;
  background: rgb(106, 248, 118);
  color: black;
}
</style>