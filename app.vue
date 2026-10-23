<script setup lang="ts">
// Nuxt 3 automatically auto-imports all components inside components/
</script>

<template>
  <div class="pororo-app">
    <!-- Global Centered Floating Navbar (follows across ALL sections) -->
    <Navbar />

    <!-- 1. Hero Section -->
    <HeroSection />

    <!-- 2. Favorite Flavors -->
    <FavoriteFlavors />

    <!-- 3. Ingredient Promise -->
    <IngredientPromise />

    <!-- 4. Weekend Promotion -->
    <WeekendPromotion />

    <!-- 5. Craft Process -->
    <CraftProcess />

    <!-- 6. Customer Stories -->
    <CustomerStories />

    <!-- 7. Store Location -->
    <StoreLocation />

    <!-- 8. Order Call to Action -->
    <OrderCta />

    <!-- 9. Site Footer -->
    <SiteFooter />

    <!-- Interactive Smartphone Mode Toggle -->
    <DeviceToggle />
  </div>
</template>

<style scoped>
.pororo-app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
