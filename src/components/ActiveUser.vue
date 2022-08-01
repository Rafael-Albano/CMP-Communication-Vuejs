<template>
    <section>
        <h2>{{userName}}</h2>
        <h3>{{(userAge != '') ? `${userAge} Years Old.`: ''}} </h3>
    </section>
</template>
    
<script>
export default {
    name: 'active-user',
    props: {
        userName: {
            type: String,
            required: true,
        },

        userAge: {
            type: Number,
            required: true,
        }
    },
}
</script>
