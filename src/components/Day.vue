<template>
    <div class="cell">
        {{dayOfMonth}}
    </div>
</template>

<script>
  export default {
    name: "Day",
    props: [
      'dayOfMonth',
      'dayDescOfWeek'
    ]
  }
</script>

<style>
.cell {
    border: 1em solid cadetblue;
}
</style>
