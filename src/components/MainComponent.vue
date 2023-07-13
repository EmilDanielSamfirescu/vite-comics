<script >
export default {
    name: "MainComponent",
data (){
    return {

    }
},
methods: {

}
};
</script>

<template>
    <main>
        MAIN
    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

main {
    @include debug-1;
}

</style>