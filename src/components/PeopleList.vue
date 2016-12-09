<template>
  <ul>
    <li v-for='person in people'>
      <person :person="person"></person>
    </li>
  </ul>
</template>
<script>
  import Person from 'components/Person.vue';

  export default {
    name: 'peoplelist',
    components: {
      person: Person
    },
    data: function () {
        return {
          people: this.$parent.people
        }
    }
  }
</script>
