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

<style>
    .particle-container .particle{
    position: absolute;
    height: 2.5em;
    width: 2.5em;
    border-radius: 50%;
    /*background: radial-gradient(rgb(255, 245, 153) 40%, rgb(247, 211, 51), orange, rgb(255, 81, 0));
    box-shadow: 3px 5px 10px rgba(255, 255, 255, 0.514);*/
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' class='icon icon-tabler icon-tabler-ice-cream-2' width='40' height='40' viewBox='0 0 24 24' stroke-width='2' stroke='currentColor' fill='pink' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath stroke='none' d='M0 0h24v24H0z' fill='none'/%3E%3Cpath d='M17.657 11a6 6 0 1 0 -11.315 0' /%3E%3Cpath d='M6.342 11l5.658 11l5.657 -11z' /%3E%3C/svg%3E");
    z-index: 10;
}
 
.particle-container .particle:nth-child(1){
    top: 12%;
    left: 42%;
    animation: particle-motion 1s linear infinite;
}
 
.particle-container .particle:nth-child(2){
    top: 70%;
    left: 50%;
    animation: particle-motion 7s linear infinite;
}
.particle-container .particle:nth-child(3){
    top: 17%;
    left: 6%;
    animation: particle-motion 9s linear infinite;
}
.particle-container .particle:nth-child(4){
    top: 20%;
    left: 60%;
    animation: particle-motion 10s linear infinite;
}
.particle-container .particle:nth-child(5){
    top: 67%;
    left: 10%;
    animation: particle-motion 6s linear infinite;
}
.particle-container .particle:nth-child(6){
    top: 80%;
    left: 70%;
    animation: particle-motion 11s linear infinite;
}
.particle-container .particle:nth-child(7){
    top: 60%;
    left: 80%;
    animation: particle-motion 6s linear infinite;
}
.particle-container .particle:nth-child(8){
    top: 32%;
    left: 25%;
    animation: particle-motion 6s linear infinite;
}
.particle-container .particle:nth-child(9){
    top: 90%;
    left: 25%;
    animation: particle-motion 9s linear infinite;
}
.particle-container .particle:nth-child(10){
    top: 10%;
    left: 80%;
    animation: particle-motion 5s linear infinite;
}
 
.particle-container .particle:nth-child(11){
    top: 24%;
    left: 82%;
    animation: particle-motion 10s linear infinite;
}
 
.particle-container .particle:nth-child(12){
    top: 97%;
    left: 5%;
    animation: particle-motion 7s linear infinite;
}
.particle-container .particle:nth-child(13){
    top: 97%;
    left: 60%;
    animation: particle-motion 9s linear infinite;
}
.particle-container .particle:nth-child(14){
    top: 30%;
    left: 40%;
    animation: particle-motion 5s linear infinite;
}
.particle-container .particle:nth-child(15){
    top: 47%;
    left: 55%;
    animation: particle-motion 7s linear infinite;
}
.particle-container .particle:nth-child(16){
    top: 70%;
    left: 80%;
    animation: particle-motion 8s linear infinite;
}
.particle-container .particle:nth-child(17){
    top: 40%;
    left: 40%;
    animation: particle-motion 10s linear infinite;
}
.particle-container .particle:nth-child(18){
    top: 23%;
    left: 15%;
    animation: particle-motion 4s linear infinite;
}
.particle-container .particle:nth-child(19){
    top: 90%;
    left: 90%;
    animation: particle-motion 3s linear infinite;
}
 
.particle-container .particle:nth-child(20){
    top: 85%;
    left: 95%;
    animation: particle-motion 7s linear infinite;
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
</style>