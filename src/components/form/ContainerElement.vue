<template>
    <table style="border: 1px solid gray">
        <tr v-for="item in items" v-bind:key="item.id">
            <td>
                <text-element v-if="item.type == 'text'"></text-element>
                <button-element v-if="item.type == 'button'"></button-element>
                <table-element v-if="item.type == 'table'" :items="item.items"></table-element>
            </td>
        </tr>
    </table>
</template>
<script>
import TextElement from "@/components/form/TextElement.vue"
import ButtonElement from "@/components/form/ButtonElement.vue"
import TableElement from "@/components/form/TableElement.vue"

export default {
    name: "container-element",
    components: {TextElement, ButtonElement, TableElement},
    props: ['items']
}
</script>