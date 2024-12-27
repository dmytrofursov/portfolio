<script setup>
import CollectionListWrapper from '../cards/CollectionListWrapper.vue';
import CollectionList from '../cards/CollectionList.vue';
import CollectionItem from '../cards/CollectionItem.vue';
import { buildClient } from '@datocms/cma-client-browser';

const API_TOKEN = 'b5103d578b85fd73f1c2c8235b8d12'
const client = buildClient({ apiToken: API_TOKEN });

//fetching data from cms
const allRecords = await client.items.rawList()

console.log(allRecords.data[0].attributes.company_project_logo)
</script>

<template>
    <CollectionListWrapper>
        <CollectionList listClass="experience-list">
            <CollectionItem  listItemClasses="">
                <!--<img v-for="record in allRecords" v-bind:imageSource="record.company_project_logo" src={{ imageSource }} />-->
            </CollectionItem>
        </CollectionList>
    </CollectionListWrapper>
</template>

<script>


export default {
    name: "ExperienceList",
    components: {
        CollectionItem,
        CollectionList,
        CollectionListWrapper
    },
    data() {
        return {
            src: "imageSource",
            validAttributeName: "imageSource"            
        }
    }
}
</script>