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
  <p class="overline">Built for modern use</p>
  <h2>Smarter meetings, all in one place</h2>
  <p>
    Send messages, share files, show your screen, and record your meetings — all
    in one workspace. Control who can join with invite-only team access, data
    encryption, and data export.
  </p>
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

.overline {
  text-transform: uppercase;
}
</style>
