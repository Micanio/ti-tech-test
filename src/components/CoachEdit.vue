<template>
    <button @click="showCoachEdit = !showCoachEdit">Edit</button>
    <div class="coach-edit" v-if="showCoachEdit">
        <label for="coach">
        <select name="coach" id="coach">
            <option value="Laura McGregor">Laura McGregor</option>
            <option value="Lana Orton">Lana Orton</option>
            <option value="hello test"> hello test</option>
        </select>
        </label>
        <button @click="saveCoach">Save</button>
    </div>
</template>

<script>

export default {
    name: 'CoachEdit',
    data() {
        return {
            showCoachEdit: false
        }
    },
    methods: {
        saveCoach() {
            var newCoach = document.getElementById('coach').value
            document.getElementById('coach-name').innerText = newCoach
            this.showCoachEdit = false
            console.log(newCoach)
        }
    }
}

</script>