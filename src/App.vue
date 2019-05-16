<template>
  <div id="app">
    <div class="block block-center">
      <md-datepicker v-model="date" />
      <div class="md-layout md-alignment-top-center">
        <md-button @click="setNull">SET NULL</md-button>
        <md-button @click="setDefault">SET DEFAULT</md-button>
        <md-button @click="setCurrent">SET CURRENT</md-button>
      </div>
    </div>
  </div>
</template>

<script>
const date = new Date;
export default {
  name: 'app',
  data() {
    return {
        defaultDate: date,
        date: date,
      };
    },
  components: {
  },
  methods: {
    setNull() {
      this.date = null;
    },
    setDefault() {
      this.date = this.defaultDate;
    },
    setCurrent() {
      this.date = new Date;
    }
  }
}
</script>

<style>
  #app {
    display: flex;
    justify-content: center;
  }

  .block-center {
    width: 500px;
  }
</style>
