<template>
        <table border="1">
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
    props: ['items'],
    data() {
        return {
            // items: 
            // [
            //     {id: 1, type: "text"},
            //     {id: 2, type: "button"}, 
            //     {id: 3, type: "button"},
            //     {id: 4, type: "text"},
            //     {id: 5, type: "text"},
            //     {id: 6, type: "button"},
            //     {id: 7, type: "table"}
            // ]
        };
    },
    created() {
        console.log(this.items);
    }
}
</script>