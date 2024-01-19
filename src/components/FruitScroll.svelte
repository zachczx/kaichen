<script>
import Pineapple from "$lib/assets/gabriel-yuji-Kr6Z_AbeItk-unsplash.webp";
import Grapes from "$lib/assets/luca-j-sNN1zPDooIg-unsplash.webp";
import Oranges from "$lib/assets/alice-pasqual-MRnV51_Yqqk-unsplash.webp";
import Watermelon from "$lib/assets/cody-chan-802n4MChUYk-unsplash.webp";
import Blueberries from "$lib/assets/nadeykina-evgeniya-epeLqDQh2PE-unsplash.webp";
import Strawberries from "$lib/assets/olga-kudriavtseva-CL26_lT3Ygg-unsplash.webp";
import Apples from "$lib/assets/annie-spratt-hiDnpd-p-eE-unsplash.webp";
</script>

<div id="fruit">
<ul>
    <li><img src="{Pineapple}" alt="Pineapple" /><span>Pineapple</span></li>
    <li><img src="{Grapes}" alt="Grape" /><span>Grape</span></li>
    <li><img src="{Oranges}" alt="oranges" /><span>Orange</span></li>
    <li><img src="{Watermelon}" alt="Watermelon" /><span>Watermelon</span></li>
    <li><img src="{Blueberries}" alt="Blueberries" /><span>Blueberries</span></li>
    <li><img src="{Strawberries}" alt="Strawberries" /><span>Strawberries</span></li>
    <li><img src="{Apples}" alt="Apples" /><span>Apples</span></li>
    <li style="background-color: black"></li>
    <li style="background-color: black"></li>
    <li style="background-color: black"></li>
</ul>
</div>

<style>
:root {
  scrollbar-color: green white;
  scrollbar-width: thin;
}

/* WebKit and Chromiums */
::-webkit-scrollbar {
  width: 0.5em;
  height: 0.3em;
  background-color: white;
}

::-webkit-scrollbar-thumb {
  background: green;
  border-radius: 5px;
}

#fruit {
  font-weight: 700;
  letter-spacing: 0.2em;
  font-size: 1.5em;
}

ul {
  list-style: none;
  width: min(90vw, 71rem);
  max-width: 71rem;
  display: flex;
  overflow-x: scroll;
  overflow-y: hidden;
  padding-bottom: 0.2rem;
}

li {
  flex: 0 0 45vw;
  max-width: 18rem;
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  height: 20rem;
}

li:nth-child(2) {
    left: 2.5rem;
}
li:nth-child(3) {
    left: 5rem;
}
li:nth-child(4) {
    left: 7.5rem;
}
li:nth-child(5) {
    left: 10rem;
}
li:nth-child(6) {
    left: 12.5rem;
}
li:nth-child(7) {
    left: 15rem;
}
li:nth-child(8) {
    left: 17.5rem;
}

span {
    position: absolute;
    color: white;
    top: 0;
    left: 0;
    display: block;
    padding: 0.2em;
    height: 100%;
    writing-mode: vertical-lr;
    text-align: center;
    transform: rotate(180deg);
}

span::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 0%;
    transform: translate(0%, -50%);
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: -1;
}

#fruit img {
    display: block;
    height: 20rem;
    width: 100%;
    object-fit: cover;
    position: absolute;
    top: 50%;
    left: 0;
    transform: translate(0%, -50%);
    z-index: -2;
}
</style>