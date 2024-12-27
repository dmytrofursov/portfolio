<script setup>
import CollectionListWrapper from '../cards/CollectionListWrapper.vue';
import CollectionList from '../cards/CollectionList.vue';
import CollectionItem from '../cards/CollectionItem.vue';
import CompanyLogo from '../cards/CompanyLogo.vue';
import { buildClient } from '@datocms/cma-client-browser';

const API_TOKEN = 'b5103d578b85fd73f1c2c8235b8d12'
const client = buildClient({ apiToken: API_TOKEN });

//fetching data from cms
const allRecords = await client.items.rawList()

console.log(allRecords)
</script>

<template>
    <CollectionListWrapper>
        <CollectionList listClass="experience-list">
            <CollectionItem v-for="record in allRecords" listItemClasses="">
                <CompanyLogo sourceImg={{record.company_project_logo }} />
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
        CollectionListWrapper,
        CompanyLogo
    }
}
</script>