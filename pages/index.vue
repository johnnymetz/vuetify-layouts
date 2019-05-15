<template>
  <div>
    <HtmlTags/>
    <hr>
    <Playground/>
    <hr>
    <GrowShrink/>
    <hr>
    <NestedGrid/>
    <hr>
    <NestedGridDocs/>
    <hr>
    <UniqueLayout/>
  </div>
</template>

<script>
import HtmlTags from "@/components/HtmlTags.vue";
import Playground from "@/components/Playground.vue";
import GrowShrink from "@/components/GrowShrink.vue";
import NestedGrid from "@/components/NestedGrid.vue";
import NestedGridDocs from "@/components/NestedGridDocs.vue";
import UniqueLayoutDocs from "@/components/UniqueLayoutDocs.vue";

export default {
  components: {
    HtmlTags,
    Playground,
    GrowShrink,
    NestedGrid,
    NestedGridDocs,
    UniqueLayoutDocs
  }
};
</script>

<style>
hr {
  margin: 20px 0;
}
</style>

