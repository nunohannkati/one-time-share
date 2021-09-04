<template>
  <div class="broadcastContainer">
    <h3 class="broadcastTitle">配信中</h3>
    <div class="broadcastArea">
      <div class="niconico">準備中</div>
      <div id="twitch" class="twitch"></div>
      <div class="youtube">準備中</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Broadcast",
  mounted() {
    let player = new Twitch.Player("twitch", {
      channel: "nunohannkati",
      width: "100%",
      height: "100%",
    });
    player.setVolume(0.0);
    player.addEventListener(Twitch.Player.PAUSE, () => {
      console.log("Player is paused!");
    });
  },
};
</script>

<style scoped>
.broadcastContainer {
  background-color: #f67690;
  border-radius: 5px;
  margin: 2px 2px 2px 2px;
}

.broadcastTitle {
  font-size: 20px;
  margin: 0;
  margin-left: 4px;
}

.broadcastArea {
  height: 161px;
  display: flex;
  justify-content: space-around;
  gap: 8px;
}

.niconico {
  background-color: #ffffff;
  width: 272px;
  height: 153px;
}

.twitch {
  background-color: #ffffff;
  width: 272px;
  height: 153px;
}

.youtube {
  justify-self: end;
  background-color: #ffffff;
  width: 272px;
  height: 153px;
}
</style>