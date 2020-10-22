<template>
    <div class="container">
        <div>
            <h1 class="title">
                nuxt
                {{ ip }}
            </h1>
            <div class="links"></div>
        </div>
    </div>
</template>

<script>
export default {
    async asyncData({ $axios }) {
        const ip = await $axios.$get('http://localhost:3000/api/users/login');
        console.log(ip);
        return { ip };
    }
};
</script>
