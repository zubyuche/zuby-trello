<script></script>

<template>
  <div class="container">
    <div class="new-card">
      <p class="add-card-text">+ New card</p>
    </div>
  </div>
</template>

<style>
.container {
  display: flex;
  justify-content: center;
  width: 260px;
  margin-left: 8px;
}
.add-card-text {
  font-size: 14px;
}

.new-card {
  display: flex;
  height: 20px;
  width: 100%;
  border-radius: 5px;
  cursor: pointer;
  align-items: center;
  padding: 4px 8px;
  border: none;
  outline: inherit;
  background-color: gray;
}
.new-card:hover {
  opacity: 0.5;
}
</style>