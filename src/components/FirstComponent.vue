<template>
    <div>
        <div>first component!</div>
        <second-component v-if="show"/>
    </div>
    
</template>

<script lang="ts">
import Vue from 'vue'
import SecondComponent from './SecondComponent.vue'

const mixin = {
    props: {
        show: {
            type: Boolean
        }
    }
};

export default Vue.extend({
    components: {
        SecondComponent
    },
    mixins: [mixin]
})
</script>