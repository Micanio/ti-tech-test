<template>
    <div class="bundles">
        <div class="bundle" v-for="bundle in bundles" :key="bundle.id">
            <h2></h2>
            <div class="coach"></div>
            <div class="duration"></div>
            <div class="deadline"></div>
            <div class="session"></div>
        </div>
    </div>
</template>

<script>
import json from '../assets/bundles.json'

export default {
    name: 'Bundle',
    data() {
        return {
            bundle: json
        }
    }, 
    computed: {
        bundles() {
            return this.bundle
        }
    }
}


</script>