<template>
    <div class="bundles">
        <div class="bundle" v-for="bundle in bundles" :key="bundle.id">
            <h2>{{ bundle.user.first_name }} {{ bundle.user.last_name }}</h2>
            <div class="coach">
                <p>Coach: {{ bundle.coach.first_name }} {{ bundle.coach.last_name }}</p>
            </div>
            <div class="duration">
                <p>Duration: {{ bundle.duration_mins }} mins</p>
            </div>
            <div class="deadline">
                <p>Deadline: {{ bundle.deadline }}</p>
            </div>
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

<style>
.bundles {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.bundle {
    margin: 20px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    flex-basis: 30%;
}
</style>