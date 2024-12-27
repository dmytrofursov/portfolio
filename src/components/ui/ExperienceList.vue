<script setup>
import CollectionListWrapper from '../cards/CollectionListWrapper.vue';
import CollectionList from '../cards/CollectionList.vue';
import CollectionItem from '../cards/CollectionItem.vue';
import CompanyLogo from '../cards/CompanyLogo.vue';
import { buildClient } from '@datocms/cma-client-browser';

const API_TOKEN = 'b5103d578b85fd73f1c2c8235b8d12'
const client = buildClient({ apiToken: API_TOKEN });

//fetching data from cms
Vue.prototype.$allRecords = await client.items.rawList()

console.log(allRecords)
</script>

<template>
    <CollectionListWrapper>
        <CollectionList listClass="experience-list">
            <CompanyLogo listItemClass="" v-for="record in allRecords" :imageSource="record.company_project_logo" sourceImg={{ imageSource }} />
            <!--
            <CollectionItem  listItemClasses="">
                <CompanyLogo v-for="record in allRecords" :imageSource="record.company_project_logo" sourceImg={{imageSource }} />
            </CollectionItem>
            -->
        </CollectionList>
    </CollectionListWrapper>
</template>

<script>


export default {
    name: "ExperienceList",
    components: {
        CollectionItem,
        CollectionList,
        CollectionListWrapper,
        CompanyLogo
    }
}
</script>