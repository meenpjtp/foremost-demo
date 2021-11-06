<template>
    <button :class="[shadow ? 'button-general shadow' : 'button-general']">{{ name }}</button>
</template>

<script>
export default {
    props: ['shadow', 'name']
}
</script>