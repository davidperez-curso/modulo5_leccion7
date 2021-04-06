<template>
    <b-container>
        <b-jumbotron header="BootstrapVue" lead="Bootstrap v4 Components for Vue.js 2">
            <p>For more information visit website</p>
            <b-button variant="primary" href="https://bootstrap-vue.org/">More Info</b-button>
        </b-jumbotron>
        <b-form-group horizontal:label-cols="4" description="Ingrese su nombre." label="Ingrese su nombre">
            <b-form-input v-model.trim="name"></b-form-input>
        </b-form-group>
        <b-alert variant="success" :show="showAlert">Hola {{ name }}</b-alert>
    </b-container>
</template>

<script>
export default {
    data(){
        return{
            name: ""
        }
    },
    computed: {
        showAlert(){
            return this.name.length > 4 ? true : false
        }
    }
}
</script>

<style>

</style>