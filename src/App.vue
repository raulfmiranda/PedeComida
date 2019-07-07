<template>
    <div>
        <app-header></app-header>
        <div class="container">
            <div class="row">
                <div class="col s12 m12">
                    <span v-for="opcao in opcoesEscolhidas"> {{ opcao }}, </span>
                </div>
            </div>
        </div>
        <form action="#" class="container">
            <div v-for="(escolha, index) in cardapio.escolhas" class="row">
                <div class="col s12 m12">
                    <div class="card blue-grey darken-1">
                        <div class="card-content white-text">
                            <span class="card-title">{{ index + 1 }}ª Escolha</span>
                            <!-- <p>CARNE BOVINA</p> -->
                            <label v-for="opcao in escolha">
                                <input :id="opcao.id" @change="escolhe" type="checkbox" class="filled-in" />
                                <span>{{ opcao.id }} {{ opcao.nome }}</span>
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
    data: function() {
        return {
            cardapio: {
                escolhas: [
                    [
                        { id: 1, nome: 'Escondidinho de Carne de sol' },
                        { id: 6, nome: 'Bisteca bovina na chapa' },
                        { id: 7, nome: 'Picadinho de carne c/ linguiça e batatas' },
                        { id: 23, nome: 'Costelinha na brasa' }
                    ],
                    [
                        { id: 28, nome: 'Corda c/ linguiça defumada' }
                    ],
                    [
                        { id: 31, nome: 'Farofa de Lombo Picadinho' },
                        { id: 32, nome: 'Farofa de torresmo' },
                        { id: 33, nome: 'Farofa de manteiga' }
                    ],
                    [
                        { id: 34, nome: 'Arroz branco soltinho' }
                    ],
                    [
                        { id: 41, nome: 'Batata sauté' }
                    ]
                ]
            },
            opcoesEscolhidas: []
        };        
    },
    methods: {
        escolhe(event) {
            if (!this.opcoesEscolhidas.includes(event.target.id)) {
                this.opcoesEscolhidas.push(event.target.id);
            } else {
                const index = this.opcoesEscolhidas.indexOf(event.target.id);
                this.opcoesEscolhidas.splice(index, 1);
            }
        }
    },
    components: {
        appHeader: Header
    }
};
</script>

<style>
</style>
