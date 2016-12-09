<template>
  <div>
        <h1><img :src="person.picture" :alt="person.name"> {{ person.name }}</h1>
        <h3>{{ person.company }}</h3>
        <ul>
            <li>Age: {{ person.age }}</li>
            <li>Eye Colour: {{ person.eyeColor }}</li>
            <li>Email: <a :href="'mailto:' + person.email">{{ person.email }}</a></li>
        </ul>
        <h4>Address</h4>
        <p>{{ person.address }}</p>
        <h4>About {{ person.name }}</h4>
        <p>{{ person.about }}</p>

        <router-link :to="{ name: 'home' }" class='button is-primary'>Home</router-link>
    </div>
</template>
<script>
  export default {
    name: 'persondetail',
    data: function () {
        return {
          people: this.$parent.people,
          person: {}
        }
    },
    created() {
      let guid = this.$route.params.id;

      let filtered = this.people.filter((item, index) => {
        return item.guid == guid;
      });
      this.person = filtered[0];
    }
  }
</script>
