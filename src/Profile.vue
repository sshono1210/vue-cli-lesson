<template>
    <div>
        <p>name: {{user}}</p>
        <p>age: 18</p>
    </div>
</template>

<script>
    export default{
        name: "profile",
        data(){
            return {
                user: "John"
            }
        }
    }
</script>