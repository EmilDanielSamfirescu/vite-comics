<script >
export default {
    name: "FooterComponent",
data (){
    return {

    }
},
methods: {

}
};
</script>

<template>
    <footer>
        <section class="top-footer">top-footer</section>
        <section class="center-footer">center-footer</section>
        <section class="bottom-footer">bottom-footer</section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
.top-footer {
    background-color: $footer-bg-blue;
}
.bottom-footer {
    background-color: $footer-bg-black;
}

</style>
