<template>
  <HorizontalContainer>
    <Hero
      title="Quick start"
      description="Get a taste of Nix's power and learn key concepts along the way"
      client:load
    />

    <Grid2>
      <HoverableLink
        v-for="({ href, frontmatter }, idx) in sortedQuickStartPages"
        :key="idx"
        :href="href"
        :order="frontmatter.order"
        :text="frontmatter.title"
        size="normal"
      />
    </Grid2>
  </HorizontalContainer>
</template>

<script setup lang="ts">
import { sortedQuickStartPages } from "../../logic/content";
</script>
