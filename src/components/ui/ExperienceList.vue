<script setup>
import CollectionListWrapper from '../cards/CollectionListWrapper.vue';
import CollectionList from '../cards/CollectionList.vue';
import CollectionItem from '../cards/CollectionItem.vue';
//import CompanyLogo from '../cards/CompanyLogo.vue';
import { buildClient } from '@datocms/cma-client-node';

const APITOKEN =  'b5103d578b85fd73f1c2c8235b8d12'

const client = buildClient({
  apiToken: APITOKEN,
  lofLevel: LogLevel.BASIC
});

const allRecords = []

for await (
    const record of client.items.listPagedIterator(
        
    )
) {
    allRecords.push(record)
}

console.log(allRecords)

</script>

<template>
    <CollectionListWrapper>
        <CollectionList listClass="experience-list">
            <CollectionItem listItemClasses="">
                <!--<CompanyLogo />-->
            </CollectionItem>
        </CollectionList>
    </CollectionListWrapper>
</template>

<script>
export default {
    name: "ExperienceList"
}
</script>