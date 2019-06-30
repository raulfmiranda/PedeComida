<template>
    <div>
        <app-header></app-header>
        <form action="#" class="container">
            <div class="row">
                <div class="col s12 m12">
                    <div class="card blue-grey darken-1">
                        <div class="card-content white-text">
                            <span class="card-title">1ª Escolha</span>
                            <p>CARNE BOVINA</p>
                            <label>
                                <input type="checkbox" class="filled-in" checked="checked" />
                                <span>1 Escondidinho de Carne de sol c/ macaxeira</span>
                            </label>
                            <label>
                                <input type="checkbox" class="filled-in" />
                                <span>2 Carne de sol refogada na manteiga</span>
                            </label>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col s12 m12">
                    <div class="card blue-grey darken-1">
                        <div class="card-content white-text">
                            <span class="card-title">2ª Escolha</span>
                            <p>FEIJÃO</p>
                            <label>
                                <input type="checkbox" class="filled-in" checked="checked" />
                                <span>28 Corda c/ linguiça defumada</span>
                            </label>
                            <label>
                                <input type="checkbox" class="filled-in" />
                                <span>29 Carioca c/ calabresa</span>
                            </label>
                        </div>
                    </div>
                </div>
            </div>
        </form>
    </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
    components: {
        appHeader: Header
    }
};
</script>

<style>
</style>
