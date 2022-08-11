<template>
  <div class="grid">
    <img
      class="grid-img"
      src="../assets/desktop/image-woman-in-videocall.jpg"
      alt=""
    />
    <img
      class="grid-img"
      src="../assets/desktop/image-women-videochatting.jpg"
      alt=""
    />
    <img
      class="grid-img"
      src="../assets/desktop/image-men-in-meeting.jpg"
      alt=""
    />
    <img
      class="grid-img"
      src="../assets/desktop/image-man-texting.jpg"
      alt=""
    />
  </div>
</template>

<style scoped>
.grid-img {
  width: 100%;
  border-radius: 0.5rem;
}

.grid {
  display: grid;
  place-items: center;
  grid-template-columns: 1fr 1fr;
  column-gap: 25px;
  row-gap: 24px;
  margin-left: 1.5rem;
  margin-right: 1.5rem;
}
</style>
