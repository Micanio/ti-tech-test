<template>
    <button @click="showDurationEdit = !showDurationEdit">Edit</button>
    <div class="duration-edit" v-if="showDurationEdit">
        <label for="duration">Change duration:</label>
        <input type="number" name="duration" id="durationValue">
        <button @click="saveDuration">Save</button>
    </div>
</template>

<script>

export default {
    name: 'DurationEdit',
    data() {
        return {
            showDurationEdit: false
        }
    },
    methods: {
        saveDuration() {
            var newDuration = document.getElementById('durationValue').value
            document.getElementById('duration').innerText = newDuration
            this.showDurationEdit = false
        }
    }
}

</script>