<template>
  <div class="c-cash-main">
    <div class="container">
      <p class="c-cash-main__text">
        PKT is a native blockchain based on bitcoin code. It has a 1 minute
        block time, uses PacketCrypt proof of work and has a Network Steward
        address which receives 20% of every coinbase payout. There are a total
        of 6 billion PKT which will be mined and rather than an abrupt halving
        of the payouts every 4 years, PKT uses a steady decay of 10% every 100
        days.
      </p>
      <figure class="c-cash-main__grafic">
        <img src="/img/cash-grafic.png" alt class="c-cash-main__grafic-img" />
        <figcaption
          class="c-cash-main__grafic-caption"
        >Payout of PKT vs. BTC as percent of total coins</figcaption>
      </figure>
      <p class="c-cash-main__text">
        Because PKT is designed for microtransactions, there will be a total of
        6 billion PKT mined whereas bitcoin will max out at 21 million.
        Furthermore, each PKT is subdividable into 1,073,741,824 units (2 to the
        30th power) whereas there are only 100 million satoshis per bitcoin.
        When the Bitcoin price reached almost $42,000 in January 2021, the price of a
        satoshi was 0.04 cents. This cost per satoshi is impractical for microtransactions, even with nearly free
        transacting over the Lightning Network.
      </p>
      <p class="c-cash-main__text">
        PKT is designed around the idea of fast cheap transacting in small denominations to enable a bandwidth trading marketplace. PKT Cash provides an economic incentive for people to connect bandwidth to the network. The Network
        Steward is designed to ensure funding is available to build-out decentralized internet infrastructure and open-source technology.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CashMain",
  props: {
    title: String,
    text: String,
    bg: String,
  },
};
</script>

<style lang="scss">
.c-cash-main {
  padding: rem(100) rem(15) rem(50);

  & .container {
    width: 100%;
    max-width: rem(1075);
    margin: 0 auto;
  }

  &__text {
    @extend %text-main;
    color: $dark_blue;


    &:not(:last-child) {
      margin-bottom: rem(28);
    }

    & br {
      height: rem(50);
    }
  }

  &__grafic {
    margin-top: rem(75);
    margin-bottom: rem(100);
    width: 100%;

    &-img {
      object-fit: cover;
      width: 100%;
      height: 100%;
    }

    &-caption {
      width: 100%;
      margin-top: rem(33);
      text-align: center;
      @extend %light;
      @include font_sizes(24, 35);
      @include for-width(-tablet) {
        @include font_sizes(14, 24);
      }
    }
  }
}
</style>
