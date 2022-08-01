<template>
    <section>
        <active-user :user-name="name" :user-age="age" />
        <user-data @submit-data="setName" />
    </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue';
import UserData from './components/UserData.vue';

export default {
    components: {
        ActiveUser,
        UserData
    }, 
    data() {
        return {
            name: '',
            age: '',
        }
    },

    methods: {
        setName(enteredName, enteredAge) {
            this.name = enteredName;
            this.age = enteredAge;
        }
    }
}
</script>

<style>
html {
  font-family: sans-serif;
}

section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem;
}
</style>
        ActiveUser