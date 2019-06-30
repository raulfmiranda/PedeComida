<template>
    <nav>
        <div class="nav-wrapper">
            <a href="#!" class="brand-logo center">
                <i class="material-icons">restaurant</i>
                {{ title }}
            </a>
        </div>
    </nav>
</template>

<script>
export default {
    data: function() {
        return {
            title: "Pede Comida"
        };
    }
};
</script>

<style scoped>
</style>
