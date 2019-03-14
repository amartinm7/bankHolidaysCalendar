<template>
    <div class="grid">
        <template v-for="(month, monthNumber) in months">
            <template v-for="(dayOfMonth) in getDaysOnMonth(monthNumber, 2019)" >
                <day v-bind:day-of-month="dayOfMonth"
                     v-bind:day-desc-of-week="getDayDescOfWeek(dayOfMonth, monthNumber, 2019)" />
            </template>
        </template>
    </div>
</template>

<script>
  import Day from "./Day";

  export default {
    name: "Month",
    components: {Day},
    data(){
      return {
        months: ['january','february','march','april','may','june','july','august','september','october','november','december'],
        daysOfWeek: ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday']
      }
    },
    methods:{
        getDaysOnMonth: function (month, year) {
          return new Date(year, month, 0).getDate();
        },
        getDayNumberOfWeek: function (dayOfMonth, month, year){
          const date = new Date(year, month, dayOfMonth);
          return date.getDay()
        },
        getDayDescOfWeek: function (dayOfMonth, month, year){
          return this.daysOfWeek[this.getDayNumberOfWeek(dayOfMonth, month, year)]
        }
    },
  }
</script>

<style >
.grid {
    display: grid;
}
</style>
