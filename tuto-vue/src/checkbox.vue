<template>
    <label for="">
        <input type="checkbox" name="" id="">
        Lorem ipsum dolor sit amet, consectetur 
        adipisicing elit. Ad corporis provident minima, 
        dolores voluptas in deserunt nulla quo dicta iusto 
        autem impedit aliquam. Aperiam, dolore sed quas 
        exercitationem quasi libero.
    </label>
</template>

<script setup>
    const props = defineProps({
        label: String
    })
    console.log(props.label)
</script>