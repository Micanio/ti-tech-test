<template>
    <div class="bundles">
        <div class="bundle" v-for="bundle in bundles" :key="bundle.id">
            <h2>{{ bundle.user.first_name }} {{ bundle.user.last_name }}</h2>
            <div class="bundle-info">
                <div class="coach">
                    <p><span class="label">Coach:</span> {{ bundle.coach.first_name }} {{ bundle.coach.last_name }}</p>
                    <CoachEdit />
                </div>
                <div class="duration">
                    <p><span class="label">Duration:</span> {{ bundle.duration_mins }} mins</p>
                </div>
                <div class="deadline">
                    <p><span class="label">Deadline:</span> {{ formatDate(bundle.deadline) }}</p>
                </div>
            </div>
            <div class="session" v-for="session in bundle.sessions" :key="session.id">
                <h3>Session {{ session.id }}</h3>
                <p>{{ formatDate(session.date) }} {{ session.type }} - {{ session.status.title }}</p>
            </div>
            
        </div>
    </div>
</template>

<script>
import json from '../assets/bundles.json'
import CoachEdit from './CoachEdit.vue'

export default {
    name: 'Bundle',
    components: {
        CoachEdit
    },
    data() {
        return {
            bundle: json
        }
    }, 
    computed: {
        bundles() {
            return this.bundle
        }
    },
    methods: {
        
        formatDate(date) {
            if (date === null) {
                return
            } else {
                return new Date(date).toLocaleDateString()
            }    
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
h2 {
    border-bottom: 1px solid #ccc;
    padding-bottom: 20px;
    text-align: center;
}
.bundle-info {
    margin-top: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 20px;
}
span.label {
    font-weight: bold;
}

</style>