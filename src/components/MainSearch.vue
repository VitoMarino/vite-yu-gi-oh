<script>

</script>

<template>
    <label for="carta"><strong>Scegli la carta:</strong></label>
    <select @click="$emit('cerca')" name="select" id="select">
        <option value="1">1</option>
        <option value="2">1</option>
        <option value="3">1</option>
        <option value="4">1</option>
    </select>
</template>

<style lang="scss" scoped>
    label {
        text-transform: uppercase;
        padding: 1rem;
    }

    select{
        padding: .3rem 1rem .3rem 1rem;
        background-color: rgb(255, 119, 0);
        border-radius: .5rem;
        border-style: none;
        margin-bottom: .5rem;
    }
</style>