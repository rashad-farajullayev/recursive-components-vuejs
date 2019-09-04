<template>
    <div style="margin-left: 120px">
        <container-element :items="items"></container-element>
    </div>
</template>
<script>
export default {
    name: "table-element",
    components: {ContainerElement: () => import('./ContainerElement.vue')},
    props: ['items']
}
</script>