<template>
    <div>
        <h1>
            Hello World from ComponentTesting
        </h1>
        <br/>
        <container-element :items="items"></container-element>        
    </div>
</template>
<script>


import ContainerElement from "@/components/form/ContainerElement.vue"

export default {
    name: "component-test",
    components: {ContainerElement},
    data() {
        return {
            items: 
            [
                {id: 1, type: "text"},
                {id: 2, type: "button"}, 
                {id: 3, type: "button"},
                {id: 4, type: "text"},
                {id: 5, type: "text"},
                {id: 6, type: "button"},
                {id: 7, type: "table", items: 
                                        [
                                            {id: 9, type: "text"},
                                            {id: 10, type: "text"},
                                            {id: 11, type: "button"},
                                            {id: 12, type: "table", items: 
                                                [
                                                    {id: 13, type: "text"},
                                                    {id: 14, type: "button"}, 
                                                    {id: 15, type: "button"},
                                                    {id: 16, type: "text"},              
                                                ]
                                            },
                                        ]},
                {id: 8, type: "button"}
            ]
        };
    }
}
</script>