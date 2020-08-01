<template>
  <div class="c-about-main">
    <div class="container">
      <h1 class="c-about-main__title">Letter from CJD</h1>
      <h2 class="c-about-main__subtitle">ARPANET Paved the Way</h2>
      <p
        class="c-about-main__text"
      >It's been just over 50 years since the US military issued the first contract to build ARPANET, the network which would eventually evolve into the Internet.</p>
      <p
        class="c-about-main__text"
      >The year was 1969: Almost everybody got the daily newspaper, typing was a skill mostly confined to secretaries, and if you wanted to communicate with someone far away you would use the telephone. The telephone system itself was something hard to imagine, in most countries there was only one provider, it was illegal to connect your own telephone to the provider's network, and a 5 minute call from New York to Los Angeles cost the equivalent of $18 in today's money.</p>
      <p
        class="c-about-main__text"
      >It's hard to overstate the impact that the Internet has had on the world. The ability of everyone to become a publisher has lead to entirely new forms of journalism and media. Teleconferencing has given rise to remote work and even entirely remote teams. E-commerce and crowdfunding combined with low volume manufacturing have given customers not only incredible choice, but direct input into what products are made. These phenomenon, while wildly futuristic by 1969 standards, would at least have been comprehensible; but open source software projects, decentralized social media, and blockchains are so far removed from that world that there wouldn't even be a basis to explain them.</p>
      <span
        class="c-about-main__quote"
      >“The Internet has probably been the biggest single force for individual liberation since the printing press.”</span>
      <p
        class="c-about-main__text"
      >At first it might look like a normal evolution of the telephone system, but when ARPANET was first devised, there was a design decision which made it fundamentally different. To a network, the protocol is like its DNA, and the DNA of the telephone network was an evolution from the days when calls were made by asking an operator to "patch you through" by plugging in a physical wire. While telephone protocols worked with only simple electronics and electromechanical switches, their limitation is they were inherently centralized.</p>
      <p
        class="c-about-main__text"
      >ARPANET on the other hand was designed to be decentralized. As a military network, resiliency was a requirement, and this decision to adopt a decentralized protocol paved the way to a cooperative/competitive inter-network of tens of thousands of service providers which has since revolutionized the world. But at the time ARPANET was nothing more than a couple of computers communicating over telephone modems.</p>
      <span
        class="c-about-main__quote"
      >“If a network has the right DNA, it doesn't matter how small it is at the beginning.”</span>
      <p
        class="c-about-main__text"
      >The core of the Internet has blossomed into a rich ecosystem, but many people are not able to effectively participate because they have limited access or no access at all. The ARPANET architecture has allowed for tens of thousands of independent network operators, but we need to lower the barrier of entry to allow for hundreds of millions of network operators.</p>
      <p
        class="c-about-main__text"
      >PKT’s plan is to separate the role of infrastructure provider (the boots-on-the-ground job of connecting fiber and pointing antennas), from the role of network operator (the complex technical job of planning routes that data should take). Between these two roles will be a decentralized bandwidth marketplace where the infrastructure providers sell bandwidth leases to the network operators.</p>
      <p
        class="c-about-main__text"
      >PKT intends to change the dynamic from pay-for-access to pay-for-priority because it makes absolutely no sense that a person should be unable to communicate while there's a perfectly good Internet connection sitting idle.</p>
      <span class="c-about-main__quote">
        "This plan is obviously very ambitious, but like ARPANET started as a couple of computers connected over the telephone,
        PKT has begun this way as well."
      </span>
      <p
        class="c-about-main__text"
      >PKT also carries forward the belief that communications should be encrypted. This means, nobody should have to apply for https certificates, there should be no question of the origins of a data packet when it is received, and nobody should ever need a VPN to get another Internet connection when they already have one.</p>
      <p
        class="c-about-main__text"
      >If you believe that the internet should be owned by the people, and that no one should ever be denied access while bandwidth sits unused, if you want to look back on the days of $50 a month the way we look back on the days of $18 phone calls, come build with us. We're just getting started.</p>
      <figure class="c-about-main__signature">
        <img src="/img/signature.png" alt="Signature" />
        <figcaption class="c-about-main__signature-name">Caleb James DeLisle</figcaption>
      </figure>
      <div class="c-about-main__btns">
        <nuxt-link class="c-about-main__btns-link blue-btn-arrow" to="/">
          <span>PKT Roadmap</span>
        </nuxt-link>
        <nuxt-link class="c-about-main__btns-link blue-btn-arrow" to="/">
          <span>PKT Origin Story</span>
        </nuxt-link>
      </div>
      <div class="c-about-main__separator"></div>
      <span class="c-about-main__involved">Get involved</span>
      <div class="c-about-main__email">
        <input type="text" placeholder="Email" class="c-about-main__email-input" />
        <button class="c-about-main__email-btn blue-btn">Join The Community</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutMain",
};
</script>

<style lang="scss">
.c-about-main {
  padding: rem(100) 0 rem(180);

  & .container {
    width: 100%;
    max-width: rem(1100);
    margin: 0 auto;
    padding: 0 rem(15);
  }

  &__title {
    @extend %h1-title;
    color: $dark_blue;
    margin-bottom: rem(40);
  }

  &__subtitle {
    @extend %h2-title;
    color: $dark_blue;
    margin-bottom: rem(60);
  }

  &__text {
    @extend %text-main;
    color: $dark_blue;
    margin-bottom: rem(15);
  }

  &__quote {
    display: block;
    @extend %italic-quote;
    color: $dark_blue;
    margin: rem(80) auto;
    max-width: 85%;
    text-align: center;
  }

  &__signature {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    margin: rem(40) rem(200) rem(60) auto;

    &-name {
      @include font_sizes(18, 20);
      color: $dark_blue;
    }
  }

  &__btns {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: rem(100);

    &-link:not(:last-child) {
      margin-right: rem(40);
    }
  }

  &__separator {
    background-color: rgba(0, 0, 0, 0.08);
    width: 100%;
    max-width: rem(285);
    height: rem(1);
    margin: 0 auto rem(100);
  }

  &__involved {
    @extend %h2-title;
    color: $dark_blue;
    display: inline-block;
    width: 100%;
    text-align: center;
  }

  &__email {
    display: block;
    position: relative;
    margin: rem(100) auto 0;
    max-width: rem(750);

    &-input {
      width: 100%;
      background-color: $dark_blue;
      padding: rem(17) rem(34);
      @include font_sizes(17, 24);
      border-radius: rem(48);
      border: none;
      color: $light_blue;

      &::placeholder {
        color: $light_blue;
        opacity: 0.8;
      }
    }

    &-btn {
      position: absolute;
      top: 0;
      right: 0;
    }
  }
}
</style>