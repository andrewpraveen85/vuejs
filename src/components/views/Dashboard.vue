<template>
  <!-- Main content -->
  <section class='content'>
    <div class='row '>
    <div class='col-md-3'>
<apexchart 
     width='500' type='bar' 
     :options='options' :series='series'>
   </apexchart>
</div>
<div class='col-md-3'>
</div>
<div class='col-md-6'></div>
</div>
    <!-- /.row -->
  </section>
  <!-- /.content -->
</template>

<script>
import '@/plugins/apexcharts'

export default {
  name: 'Dashboard',
  data: () => ({
    options: {
      chart: {
        id: 'vuechart-example'
      },
      xaxis: {categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']}
    },
    series: [{
      name: 'series-1',
      data: [55, 62, 89, 66, 98, 72, 101, 75, 94, 120, 117, 139]
    }]
  }),
  computed: {
    isMobile () {
      return (window.innerWidth <= 800 && window.innerHeight <= 600)
    }
  }
}
</script>
<style>

</style>
