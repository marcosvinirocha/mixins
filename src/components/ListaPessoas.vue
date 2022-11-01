<template>
    <div>
        <h3>Lista Pessoas</h3>
        <input type="text" placeholder="Nome da pessoa" v-model="item" />
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
    name: 'ListaPessoas',
    mixins: [listaMixins, removerItemMixin]
};
</script>