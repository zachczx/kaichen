<script>

</script>

<div class="particle-container">
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
</div>

<div class="particle-container2">
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
    <div class="particle2"></div>
</div>

<style>
.particle-container .particle{
    position: absolute;
    height: 2.5em;
    width: 2.5em;
    border-radius: 50%;
    /*background: radial-gradient(rgb(255, 245, 153) 40%, rgb(247, 211, 51), orange, rgb(255, 81, 0));
    box-shadow: 3px 5px 10px rgba(255, 255, 255, 0.514);*/
    /*background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-ice-cream-2' width='40' height='40' viewBox='0 0 24 24' stroke-width='2' stroke='currentColor' fill='pink' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath stroke='none' d='M0 0h24v24H0z' fill='none'/%3E%3Cpath d='M17.657 11a6 6 0 1 0 -11.315 0' /%3E%3Cpath d='M6.342 11l5.658 11l5.657 -11z' /%3E%3C/svg%3E");
    */
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-balloon' width='40' height='40' viewBox='0 0 24 24' stroke-width='2' stroke='currentColor' fill='red' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath stroke='none' d='M0 0h24v24H0z' fill='none'/%3E%3Cpath d='M14 8a2 2 0 0 0 -2 -2' /%3E%3Cpath d='M6 8a6 6 0 1 1 12 0c0 4.97 -2.686 9 -6 9s-6 -4.03 -6 -9' /%3E%3Cpath d='M12 17v1a2 2 0 0 1 -2 2h-3a2 2 0 0 0 -2 2' /%3E%3C/svg%3E");    z-index: 10;
}

.particle-container .particle:nth-child(1){
    top: 12%;
    left: 42%;
    animation: particle-motion 11s ease-out infinite;
}
 
.particle-container .particle:nth-child(2){
    top: 70%;
    left: 50%;
    animation: particle-motion 7s linear infinite;
}

.particle-container .particle:nth-child(3){
    top: 17%;
    left: 6%;
    animation: particle-motion 19s linear infinite;
}
.particle-container .particle:nth-child(4){
    top: 20%;
    left: 60%;
    animation: particle-motion 10s ease-in infinite;
}
.particle-container .particle:nth-child(5){
    top: 67%;
    left: 10%;
    animation: particle-motion 16s ease-out infinite;
}
.particle-container .particle:nth-child(6){
    top: 80%;
    left: 70%;
    animation: particle-motion 11s ease-in infinite;
}
.particle-container .particle:nth-child(7){
    top: 60%;
    left: 80%;
    animation: particle-motion 16s linear infinite;
}
.particle-container .particle:nth-child(8){
    top: 32%;
    left: 25%;
    animation: particle-motion 26s ease-in infinite;
}
.particle-container .particle:nth-child(9){
    top: 90%;
    left: 25%;
    animation: particle-motion 9s linear infinite;
}
.particle-container .particle:nth-child(10){
    top: 10%;
    left: 80%;
    animation: particle-motion 5s ease-in infinite;
}
 
.particle-container .particle:nth-child(11){
    top: 24%;
    left: 82%;
    animation: particle-motion 30s ease-out infinite;
}
 
.particle-container .particle:nth-child(12){
    top: 97%;
    left: 5%;
    animation: particle-motion 7s ease-in infinite;
}
.particle-container .particle:nth-child(13){
    top: 97%;
    left: 60%;
    animation: particle-motion 29s linear infinite;
}
.particle-container .particle:nth-child(14){
    top: 30%;
    left: 40%;
    animation: particle-motion 15s ease-in infinite;
}
.particle-container .particle:nth-child(15){
    top: 47%;
    left: 55%;
    animation: particle-motion 7s ease-out infinite;
}
.particle-container .particle:nth-child(16){
    top: 70%;
    left: 80%;
    animation: particle-motion 8s ease-in infinite;
}
.particle-container .particle:nth-child(17){
    top: 40%;
    left: 40%;
    animation: particle-motion 10s linear infinite;
}
.particle-container .particle:nth-child(18){
    top: 23%;
    left: 15%;
    animation: particle-motion 24s ease-out infinite;
}
.particle-container .particle:nth-child(19){
    top: 90%;
    left: 90%;
    animation: particle-motion 23s linear infinite;
}
 
.particle-container .particle:nth-child(20){
    top: 85%;
    left: 95%;
    animation: particle-motion 7s ease-out infinite;
}
 
@keyframes particle-motion {
    0%{
        transform: translate(0);
        opacity: 1;
    }
 
    20%{
        transform: translate(5px -20px);
        opacity: 0.8;
    }
 
    40%{
        transform: translate(-10px, -30px);
        opacity: 0.7;
    }
 
    60%{
        transform: translate(15px, -40px);
        opacity: 0.5;
    }
 
    80%{
        transform: translate(-20px, -60px);
        opacity: 0.2;
    }
 
    100%{
        transform: translate(40px, -100px);
        opacity: 0;
    }
}
/*-------------------------------*/


.particle-container2 .particle2{
    position: absolute;
    height: 2.5em;
    width: 2.5em;
    border-radius: 50%;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-confetti' width='40' height='40' viewBox='0 0 24 24' stroke-width='2' stroke='currentColor' fill='yellow' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath stroke='none' d='M0 0h24v24H0z' fill='none'/%3E%3Cpath d='M4 5h2' /%3E%3Cpath d='M5 4v2' /%3E%3Cpath d='M11.5 4l-.5 2' /%3E%3Cpath d='M18 5h2' /%3E%3Cpath d='M19 4v2' /%3E%3Cpath d='M15 9l-1 1' /%3E%3Cpath d='M18 13l2 -.5' /%3E%3Cpath d='M18 19h2' /%3E%3Cpath d='M19 18v2' /%3E%3Cpath d='M14 16.518l-6.518 -6.518l-4.39 9.58a1 1 0 0 0 1.329 1.329l9.579 -4.39z' /%3E%3C/svg%3E");
}

.particle-container2 .particle2:nth-child(1){
    top: 19%;
    left: 47%;
    animation: particle-motion2 25s ease-out   infinite;
}
 
.particle2-container .particle2:nth-child(2){
    top: 75%;
    left: 58%;
    animation: particle-motion2 4s linear infinite;
}

.particle-container2 .particle2:nth-child(3){
    top: 24%;
    left: 11%;
    animation: particle-motion2 19s linear infinite;
}
.particle-container2 .particle2:nth-child(4){
    top: 30%;
    left: 75%;
    animation: particle-motion2 25s ease-in infinite;
}
.particle-container2 .particle2:nth-child(5){
    top: 72%;
    left: 15%;
    animation: particle-motion2 16s ease-out infinite;
}
.particle-container2 .particle2:nth-child(6){
    top: 85%;
    left: 75%;
    animation: particle-motion2 18s ease-in infinite;
}
.particle-container2 .particle2:nth-child(7){
    top: 65%;
    left: 85%;
    animation: particle-motion2 14s linear infinite;
}
.particle-container2 .particle2:nth-child(8){
    top: 37%;
    left: 30%;
    animation: particle-motion2 21s ease-in infinite;
}
.particle-container2 .particle2:nth-child(9){
    top: 95%;
    left: 30%;
    animation: particle-motion2 9s linear infinite;
}
.particle-container2 .particle2:nth-child(10){
    top: 15%;
    left: 75%;
    animation: particle-motion2 7s ease-in infinite;
}
 
.particle-container2 .particle2:nth-child(11){
    top: 29%;
    left: 91%;
    animation: particle-motion2 30s ease-out infinite;
}
 
.particle-container2 .particle2:nth-child(12){
    top: 89%;
    left: 20%;
    animation: particle-motion2 9s ease-in infinite;
}
.particle-container2 .particle2:nth-child(13){
    top: 99%;
    left: 68%;
    animation: particle-motion2 29s linear infinite;
}
.particle-container2 .particle2:nth-child(14){
    top: 35%;
    left: 65%;
    animation: particle-motion2 15s ease-in infinite;
}
.particle-container2 .particle2:nth-child(15){
    top: 72%;
    left: 60%;
    animation: particle-motion2 11s ease-out infinite;
}
.particle-container2 .particle2:nth-child(16){
    top: 75%;
    left: 85%;
    animation: particle-motion2 8s ease-in infinite;
}
.particle-container2 .particle2:nth-child(17){
    top: 25%;
    left: 55%;
    animation: particle-motion2 20s linear infinite;
}
.particle-container2 .particle2:nth-child(18){
    top: 22%;
    left: 10%;
    animation: particle-motion2 14s ease-out infinite;
}
.particle-container2 .particle2:nth-child(19){
    top: 15%;
    left: 95%;
    animation: particle-motion2 23s linear infinite;
}
 
.particle-container2 .particle2:nth-child(20){
    top: 60%;
    left: 49%;
    animation: particle-motion2 15s ease-out infinite;
}
 
@keyframes particle-motion2 {
    0%{
        transform: translate(0);
        opacity: 1;
    }
 
    20%{
        transform: translate(5px -20px);
        opacity: 0.8;
    }
 
    40%{
        transform: translate(-11px, -33px);
        opacity: 0.7;
    }
 
    60%{
        transform: translate(15px, -40px);
        opacity: 0.5;
    }
 
    80%{
        transform: translate(-25x, -80px);
        opacity: 0.2;
    }
 
    100%{
        transform: translate(30px, -100px);
        opacity: 0;
    }
}
</style>