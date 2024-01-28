<script>
let birthday = new Date("Feb 1, 2024 00:00:00").getTime()
let days, hours, minutes, seconds
let x = setInterval(() => {
    let now = new Date().getTime()
    let difference = birthday - now

    days = Math.floor(difference / (1000 * 60 * 60 * 24));
    hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
    seconds = Math.floor((difference % (1000 * 60)) / 1000);

    if (difference<0) {
        clearInterval(x)
    }
}, 1000)
</script>

<div class="grid lg:grid-cols-1">   
        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-mood-kid fill-orange-100 stroke-orange-500" width="300" height="300" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0" />
            <path d="M9 10l.01 0" />
            <path d="M15 10l.01 0" />
            <path d="M9.5 15a3.5 3.5 0 0 0 5 0" />
            <path d="M12 3a2 2 0 0 0 0 4" />
        </svg>
</div>
<h1 class="mb-8">Hello! <!--<span class="underline decoration-red-300 underline-offset-3">Kai's</span> a toddler.--> <span class="bg-gradient-to-r from-yellow-200 via-green-200 to-pink-300 text-transparent bg-clip-text">Kai's birthday is coming!</span></h1>

<div class="grid lg:grid-cols-4 sm:grid-cols-3 gap-2">
    <div class="card w-40 bg-base-100 hover:bg-red-500 shadow-xl">
        <div class="card-body items-center text-center">
            <h2 class="card-title text-5xl">{days}</h2>
            <p>days</p>
        </div>
    </div>
    <div class="card w-40 bg-base-100 hover:bg-red-500 shadow-xl">
        <div class="card-body items-center text-center">
            <h2 class="card-title text-5xl">{hours}</h2>
            <p>hours</p>
        </div>
    </div>
    <div class="card w-40 bg-base-100 hover:bg-red-500 shadow-xl">
        <div class="card-body items-center text-center">
            <h2 class="card-title text-5xl">{minutes}</h2>
            <p>minutes</p>
        </div>
    </div>
    <div class="card w-40 bg-base-100 hover:bg-red-500 shadow-xl">
        <div class="card-body items-center text-center">
            <h2 class="card-title text-5xl ">{seconds}</h2>
            <p>seconds</p>
        </div>
    </div>
</div>