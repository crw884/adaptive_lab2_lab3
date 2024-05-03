<script setup>
    import VHeader from "@/components/VHeader.vue";
    import VPromo from "@/components/VPromo.vue";
    import VClass from "@/components/VClass.vue";
    import VHistory from "@/components/VHistory.vue";
    import VPossibilities from "@/components/VPossibilities.vue";
    import VPossibilitiesmb from "@/components/VPossibilitiesmb.vue";
    import VIdeas from "@/components/VIdeas.vue";
    import VReviews from "@/components/VReviews.vue";
    import VFooter from "@/components/VFooter.vue";
</script>

<template>
    <v-header/>
    <main>
        <v-promo></v-promo>
        <v-class></v-class>
        <v-history></v-history>   
        <v-possibilities></v-possibilities>
        <v-possibilitiesmb></v-possibilitiesmb>
        <v-ideas></v-ideas>
        <v-reviews></v-reviews>
    </main>
    <v-footer/>     
</template>

<style scoped>

</style>
