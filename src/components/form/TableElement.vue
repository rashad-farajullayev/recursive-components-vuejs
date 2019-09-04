<template>
        <table border="1">
            <tr>
                <td>
                    <!-- <h1>THIS IS TABLE</h1> -->
                    <container-element-place :items="items"></container-element-place>
                </td>
            </tr>
        </table>
</template>
<script>

import ContainerElementPlace from "@/components/form/ContainerElement.vue"
export default {
    name: "TableElement",
    components: {ContainerElementPlace},
    props: ['items'],
    created() {
        console.log("Table items: ");
        console.log(this.items);

    }
}
</script>