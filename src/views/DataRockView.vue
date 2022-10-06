<template>
  <div>
    <h1>This is a Data Rocks</h1>
    <Pivot report="https://cdn.webdatarocks.com/reports/report.json" toolbar>
    </Pivot>
  </div>
</template>

<script>
import Pivot from "@/components/Pivot";
export default {
  name: "App",
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Pivot,
  },
};
</script>

<style></style>
