<template lang="pug">
  div
    p {{ name }}
    p I am {{ age }} years old
    h1 Second Person
    p {{ person.name }}
    p {{ person.age }}
    ul
      li(v-for="friend in person.friends") {{ friend }}
</template>

<script lang="ts">
import Person from '../models/Person'

export default {
  props: {
    name: String,
    age: Number,
    person: Person
  }
};
</script>
