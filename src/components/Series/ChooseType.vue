<template>
  <section id="choose-type">
    <div>
      <a href="#" @click.prevent="chooseType(SERIES_TYPE_2_PLAYER)">2 Player Game</a><br />
      You'll start the game as player X and get a special link to invite a friend.
    </div>
    <div>or</div>
    <div>
      <a href="#" @click.prevent="chooseType(SERIES_TYPE_1_PLAYER_EASY)">Vs Computer</a><br />
      You'll start playing against your very fine computer or mobile phone.
    </div>
  </section>
</template>

<script>
import { SERIES_TYPE_2_PLAYER, SERIES_TYPE_1_PLAYER_EASY } from "@/SeriesTypes";

export default {
  data() {
    return {
      SERIES_TYPE_2_PLAYER,
      SERIES_TYPE_1_PLAYER_EASY,
    };
  },

  methods: {
    chooseType(style) {
      this.$emit("type-chosen", style);
    },
  },
};
</script>

<style lang="scss">
#choose-type {
  a {
    color: $x;
    font-size: 2rem;
  }
  div {
    line-height: 1.5;
    color: #aaaaaa;
    &:not(:last-of-type) {
      margin-bottom: 3rem;
    }
  }
}
</style>
