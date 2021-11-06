<template>
    <button class="button-capsule">
        <div :style="`backgroundImage: url(${require(`~/assets/image/${img}`)})`"></div>
        <div>
            <span>{{title}}</span>
            <p>{{text}}</p>
        </div>
    </button>
</template>

<script>
export default {
    props: ['img', 'title', 'text']
}
</script>