<template>
    <button @click="showDurationEdit = !showDurationEdit">Edit</button>
    <div class="duration-edit" v-if="showDurationEdit">
        <label for="duration">Change duration:</label>
        <input type="number" name="duration" id="duration">
        <button>Save</button>
    </div>
</template>

<script>

export default {
    name: 'DurationEdit',
    data() {
        return {
            showDurationEdit: false
        }
    }
}

</script>