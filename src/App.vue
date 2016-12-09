<template>
    <div class="columns" id="app">
      <div class='column is-6 is-offset-one-quarter'>
        <div class='content'>
          <h1>Vue Router Example</h1>
          <router-view class="view"></router-view>
        </div>
      </div>
    </div>
</template>

<script>
import PeopleList from './components/PeopleList.vue';
import 'bulma/css/bulma.css';

export default {
  name: 'app',
  components: {
    "people-list": PeopleList
  },
  data: function () {
    return {
      people: this.$parent.people
    }
  }
}
</script>

<style>
</style>
