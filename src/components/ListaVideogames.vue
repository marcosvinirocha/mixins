<template>
    <div>
        <h3>Lista Videogames</h3>
        <input type="text" placeholder="Nome do Videogame" v-model="item" />
        <button @click="adicionarItem" type="button">adicionar</button>
        <br />
        <ul>
            <li v-for="(item, index) in items" :key="index">{{ item }}</li>
        </ul>
        <button type="button" @click="removerItem">Remover</button>
    </div>
</template>

<script>
import listaMixins from '../mixins/listaMixins';
import removerItemMixin from '../mixins/removerItemMixin';


export default {
    name: 'ListaVideogame',
    mixins: [listaMixins, removerItemMixin]
};
</script>