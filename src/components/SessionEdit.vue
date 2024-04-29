<template>
    <button @click="showSessionEdit = !showSessionEdit">Edit</button>
    <div class="session-edit" v-if="showSessionEdit">
        <label for="date">Change date:</label>
        <input type="date" name="date" id="date">
        <label for="status">Change status:</label>
        <select name="status" id="status">
            <option value="status1">Unbooked</option>
            <option value="status2">Booked</option>
            <option value="status3">Completed</option>
            <option value="status4">Forfeited</option>
            <option value="status5">Void</option>
        </select>
        <button>Save</button>
    </div>
</template>

<script>

export default {
    name: 'SessionEdit',
    data() {
        return {
            showSessionEdit: false
        }
    }
}

</script>