<template>
    <div class="grid md:grid-cols-2 gap-4">
        <div class="shadow-md bg-blue-500 p-10 text-center rounded">
            <h3 class="text-3xl text-white font-bold mb-4">Cases</h3>
            <div class="text-2xl mb-4">
                <span class="font-bold text-white">New: </span>
                
                {{ numberWithCommas(stats.NewConfirmed) }}
                
            </div>
             <div class="text-2xl mb-4">
                <span class="font-bold text-white">Total: </span>
                {{ numberWithCommas(stats.TotalConfirmed)}}
                
            </div>
        </div>
          <div class="shadow-md bg-blue-500 p-10 text-center rounded">
            <h3 class="text-3xl text-white font-bold mb-4">Deaths</h3>
            <div class="text-2xl mb-4">
                <span class="font-bold text-white">New: </span>
                {{ numberWithCommas(stats.NewDeaths)}}
                
            </div>
             <div class="text-2xl mb-4">
                <span class="font-bold text-white">Total: </span>
                {{ numberWithCommas(stats.TotalDeaths)}}
                
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'DataBoxes',
    props: ['stats'],

    methods: {
        numberWithCommas(x) {
            return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
        }
    }
}
</script>
