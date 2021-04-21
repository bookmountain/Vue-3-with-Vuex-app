<template>
  <section>
    <BaseCard>
      <h1>Register as a coach now !</h1>
      <CoachForm @save-data="saveData"></CoachForm
    ></BaseCard>
  </section>
</template>

<script>
import CoachForm from '../../components/coaches/CoachForm.vue';
export default {
  components: {
    CoachForm
  },
  methods: {
    saveData(data) {
      this.$store.dispatch('coaches/registerCoach', data);
      this.$router.replace('/coaches');
    }
  }
};
</script>
