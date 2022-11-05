<script></script>

<template>
  <header>
    <div id="logo">
      <img src="@/assets/zrello1.png" />
      <p class="logo">Zrello</p>
    </div>
  </header>
</template>

<style>
header {
  width: 100%;
  background-color: var(--color-header);
  height: 50px;
  display: flex;
  justify-content: flex-start;
}
img {
  width: 90%;
  height: 90%;
  object-fit: contain;
}
#logo {
  width: 70px;
  height: 40px;
  margin-left: 20px;
  display: flex;
  justify-content: center;
  margin-top: 5px;
  border-radius: 5px;
  cursor: pointer;
}
.logo{
    font-weight: bolder;
    font-size: 30px;
    font-style: italic;
    font-family: Brush Scr;
    color: white;
    margin-top: 0%;
}
#logo:hover {
  background-color: hsla(0, 0%, 100%, 0.3);
}
</style>