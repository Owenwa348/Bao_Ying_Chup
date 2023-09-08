<!-- JaVa -->
<script setup>
import { ref } from 'vue';

const playerScore_1 = ref(0);
const playerScore_2 = ref(0);
const Scoreboard = ref('');

function playerChoice_1() {
  const choice_1 = ['ค้อน','กระดาษ','กรรไกร','ความรัก']
  return choice_1[Math.floor(Math.random() * choice_1.length)]
}
function playerChoice_2(){
  const choice_2 = ['ค้อน','กระดาษ','กรรไกร','ความรัก']
  return choice_2[Math.floor(Math.random() * choice_2.length)]
}
function start() {
  const choice_1 = playerChoice_1();
  const choice_2 = playerChoice_2();
  
  if (choice_1 === 'ค้อน' && choice_2 === 'กรรไกร') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! ค้อน vs กรรไกร';
    playerScore_1.value++;
  }else if(choice_1 === 'กระดาษ' && choice_2 === 'ค้อน') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! กระดาษ vs ค้อน';
    playerScore_1.value++;
  }else if(choice_1 === 'กรรไกร' && choice_2 === 'กระดาษ') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! กรรไกร vs กระดาษ';
    playerScore_1.value++;
  }else if (choice_1 === 'ความรัก' && choice_2 === 'กระดาษ') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! ความรัก vs กระดาษ';
    playerScore_1.value++;
  } else if (choice_1 === 'ความรัก' && choice_2 === 'ค้อน') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! ความรัก vs ค้อน';
    playerScore_1.value++;
  } else if (choice_1 === 'ความรัก' && choice_2 === 'กรรไกร') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓵ Win!!! ความรัก vs กรรไกร';
    playerScore_1.value++;
  } else if (choice_1 === 'ค้อน' && choice_2 === 'กระดาษ') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! ค้อน vs กระดาษ';
    playerScore_2.value++;
  } else if (choice_1 === 'กระดาษ' && choice_2 === 'กรรไกร') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! กระดาษ vs กรรไกร';
    playerScore_2.value++;
  } else if (choice_1 === 'กรรไกร' && choice_2 === 'ค้อน') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! กรรไกร vs ค้อน';
    playerScore_2.value++;
  } else if (choice_1 === 'ความรัก' && choice_2 === 'กระดาษ') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! ความรัก vs กระดาษ';
    playerScore_2.value++;
  } else if (choice_1 === 'ความรัก' && choice_2 === 'ค้อน') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! ความรัก vs ค้อน';
    playerScore_2.value++;
  } else if (choice_1 === 'ความรัก' && choice_2 === 'กรรไกร') {
    Scoreboard.value = '𝕡𝕝𝕒𝕪𝕖𝕣 ⓶ Win!!! ความรัก vs กรรไกร';
    playerScore_2.value++;
  } else {
    Scoreboard.value = 'เสมอ ! มันเหมือนกัน';
  }
}
function newgame() {
  playerScore_1.value = 0;
  playerScore_2.value = 0;
  Scoreboard.value = '';
}

</script>

<template>
  
<div id="game">
  <div class="ai_1">
    <header>♛King of the เป่ายิ้งฉุบ</header>
    <h1>𝕡𝕝𝕒𝕪𝕖𝕣 ⓵<span id="player_1"></span></h1>
    <img id="rock"
     src="https://media.tenor.com/W9H2Iz57nTYAAAAC/jo-jo-jjba.gif" class="logo" alt="Vite logo"/>
    <img id="paper" 
     src="https://media.tenor.com/RdLQzXxqaI0AAAAM/konan-akatsuki.gif" class="logo" alt="Vue logo"/>
    <img id="scissors" 
     src="https://media.tenor.com/KU-UzLlvhjIAAAAC/ryuko-kill-la-kill.gif" class="logo" alt="Vue logo"/> 
     
     {{ playerScore_1 }}
  </div>
  <div id="result">
    <h4>กระดานคะแนน</h4>
    {{ Scoreboard }}
  </div>
  <div class="scoresbox">
    <p id="score">คะแนน</p>
    <div class="player">
     {{ playerScore_1 }} - {{ playerScore_2 }}
    </div>
  </div>
    <h2>Vs</h2>
  <div class="ai_2">
    <h3>𝕡𝕝𝕒𝕪𝕖𝕣 ⓶<span id="player_2"></span></h3>
      <img id="rock" src="https://media.tenor.com/kHcmsxlKHEAAAAAM/rock-one-eyebrow-raised-rock-staring.gif" class="logo" alt="Vite logo"/>
      <img id="paper" src="https://media.tenor.com/KOjX2IDoOw4AAAAC/its-time-to-duel-yu-gi-oh.gif" class="logo" alt="Vue logo"/>
      <img id="scissors" src="https://38.media.tumblr.com/8add28b3994ac3fa2981d81033e899b2/tumblr_ngso0lrzhV1rp0vkjo1_500.gif" class="logo" alt="Vue logo"/>
      {{ playerScore_2 }}
  </div>
  <div class="card">
    <button @click="start">เป่ายิ้งฉุบ</button>
    <button @click ="newgame">เริ่มใหม่</button>
  </div>
</div>
</template>

<style scoped> 
*{
  background-color: #d6b27f;
}
header{
  background-color: rgb(30, 230, 230);
  color: #000;
  font-size: 30px;
  height: 45px;
}
h1{
  background-color: rgb(230, 30, 50);
  color: #ffffff;
  font-size: 25px;
  height: 35px;
}
h2{
  font-family:Fantasy;
  font-size: 50px;
  background-color: #d0b738;
  width: 70px;
  height: 70px;
  color: #ff5500;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
}
h4{
  position: absolute;
  top: 0;
  font-size: x-large;
  display: flex;
  transform: translateX(650px);
}
.player{
  position: absolute;
  top: 110px;
  font-size: x-large;
  display: flex;
  transform: translateX(650px);
}
p{
  position: absolute;
  top: 50px;
  font-size: x-large;
  display: flex;
  transform: translateX(650px);
}
h3{
  background-color: rgb(34, 31, 212);
  color: #ffffff;
  font-size: 25px;
  height: 40px;
}
h4{
  background-color: rgb(223, 200, 106);
  color: #000000;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #5d65ffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

</style>