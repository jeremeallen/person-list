<template>
  <div>
    {{person.name}}
    <router-link :to="{ name: 'person', params: { id: person.guid }}">View Details</router-link>
  </div>
</template>
<script>
  export default {
    name: 'person',
    props: [
      'person'
    ],
    data: function () {
        return {
          people: this.$parent.people
        }
    }
  }
</script>
