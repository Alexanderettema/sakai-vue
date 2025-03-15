<template>
    <div class="card">
        <div class="font-semibold text-xl mb-4c ">Empty Aexl</div>
        <Breadcrumb :model="items" class="mb-4" />
        <DataTable v-model:selection="selectedProduct" :value="products" dataKey="code" tableStyle="min-width: 50rem">
            <Column selectionMode="multiple" headerStyle="width: 3rem"></Column>
            <Column field="code" header="Code" sortable style="width: 25%"></Column>
            <Column field="name" header="Name" sortable style="width: 25%"></Column>
            <Column field="category" header="Category" sortable style="width: 25%"></Column>
            <Column field="quantity" header="Quantity" sortable style="width: 25%"></Column>
        </DataTable>
    </div>
</template>

<script>
import Breadcrumb f DataTable from 'primevue/datatable';
import { ref } from 'vue';

export default {
    components: {
        Breadcrumb,
        DataTable,
        Column
    },
    setup() {
        const items = ref([
            { label: 'Pages' },
            { label: 'Empty Aexl' }
        ]);

        const products = ref([
            {code: '1000', name: 'Product 1', category: 'Category 1', quantity: 24},
            {code: '1001', name: 'Product 2', category: 'Category 2', quantity: 54},
            {code: '1002', name: 'Product 3', category: 'Category 3', quantity: 32},
            {code: '1003', name: 'Product 4', category: 'Category 4', quantity: 62},
            {code: '1004', name: 'Product 5', category: 'Category 5', quantity: 12}
        ]);

        const selectedProduct = ref(null);

        return { items, products, selectedProduct };
    },
    name: 'EmptyPageAexl'
}
</script>

<style scoped>
h1 {
    color: navy;
}
</style>
