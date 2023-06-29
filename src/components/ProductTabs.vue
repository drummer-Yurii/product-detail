<template>
    <div class="tabs">
        <div class="tabLinks">
            <span 
                class="tab" 
                v-for="(tab, index) in tabs" 
                :key="index" 
                @click="selectedTabs = tab"
                :class="{activeTab: selectedTabs === tab}"
            >
                {{ tab }}
            </span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ProductTabs',
        data() {
            return {
                tabs: ['Reviews', 'Make a Review'],
                selectedTabs: 'Reviews'
            }
        },
    }
</script>