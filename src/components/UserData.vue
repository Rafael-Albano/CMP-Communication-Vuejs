<template>
    <form @submit.prevent="submitData">
        <input type="text" placeholder="insert your name" v-model="enteredName"/>
        <input type="text" placeholder="insert your age" v-model="enteredAge"/>
        <button type="submit">submit</button>
    </form>
</template>
    
<script>
export default {
    name: 'user-data',
    emits: ['submitData'],

    data() {
        return {
            enteredName: '',
            enteredAge: '',
        }
    },

    methods: {
        submitData() {
            this.$emit('submitData', this.enteredName, this.enteredAge);
            this.enteredName = '';
            this.enteredAge = '';
        }
    }
}
</script>

<style>

</style>