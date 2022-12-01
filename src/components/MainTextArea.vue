<template>
  <div class="main_area">
    <div class="main_text_area">
      <p class="main_text_area_top_text">
        So, you've entered your third workspace thanks to Reef, you've got your
        discount code on your food and drink and now you're ready to elevate
        your experience with FlashCharger.
        <a class="strong_and_underline" href="https://flashcharger.uk/#services"
          >Find out more about FlashCharger here.</a
        >
      </p>
    </div>
    <div class="main_context">
      <div class="main_context_text">
        <p class="main_text_area_middle_text">
          Together with Reef, Flash-Charger is offering you the opportunity to
          <span class="strong"
            >make sure you always have charge in your mobile</span
          >
          as you work from any of the collaborating Reef venues.
        </p>
        <p class="main_text_area_bottom_text">
          You've found us via The Reef App and you're ready to access your
          discount code to get portable mobile charging for less.
        </p>
        <div class="applogos">
          <a
            href="https://apps.apple.com/gb/app/flash-charger/id1540192633"
            target="_blank"
            class="appstore"
            ><img
              src="/src/assets/images/applestore.png"
              alt="Download to appstore"
          /></a>
          <a
            class="googleplay"
            href="https://play.google.com/store/apps/details?id=com.flash.charger&gl=GB&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1"
            target="_blank"
            ><img
              alt="Get it on Google Play"
              src="/src/assets/images/googleplay.png"
          /></a>
        </div>
      </div>

      <div class="flashcharger_machine">
        <img
          src="/src/assets/images/flashchargermachine.png"
          alt="a flashcharger machine"
        />
      </div>
    </div>
    <button @click="getCode">CLICK TO GENERATE PROMOTION CODE</button>
    <div class="code_group">
      <svg viewBox="0 0 53 60" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M0.275002 3.48805L11.788 26.7027C12.098 27.3271 12.14 28.0838 11.902 28.7488L1.973 56.5595C1.242 58.6068 3.163 60.5659 4.818 59.4599L51.696 28.1453C53.129 27.1878 52.999 24.7389 51.475 23.9938L2.785 0.190748C1.02 -0.671588 -0.679998 1.56143 0.275002 3.48805Z"
          fill="white"
        />
      </svg>

      <span class="code" v-if="!code">YOUR PROMOTION CODE HERE</span>
      <span class="code" v-if="code">{{ code }}</span>
      <svg viewBox="0 0 54 60" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M53.2579 56.2914L41.7449 33.0768C41.4349 32.4524 41.3929 31.6957 41.6309 31.0307L51.56 3.22001C52.291 1.17269 50.37 -0.786432 48.715 0.319634L1.83797 31.6353C0.404966 32.5928 0.534974 35.0417 2.05897 35.7869L50.7479 59.5899C52.5139 60.4511 54.214 58.2181 53.2579 56.2914Z"
          fill="white"
        />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      months: {
        jan: "FCREEF1HR01",
        feb: "FCREEF1HR02",
        mar: "FCREEF1HR03",
        apr: "FCREEF1HR04",
        may: "FCREEF1HR05",
        june: "FCREEF1HR06",
        july: "FCREEF1HR07",
        aug: "FCREEF1HR08",
        sept: "FCREEF1HR09",
        oct: "FCREEF1HR10",
        nov: "FCREEF1HR11",
        dec: "FCREEF1HR12",
      },
      code: "",
    };
  },
  methods: {
    getCode() {
      const date = new Date();
      const getCurrentMonth = date.getMonth();
      switch (getCurrentMonth) {
        case 0:
          this.code = this.months.jan;
          break;
        case 1:
          this.code = this.months.feb;
          break;
        case 2:
          this.code = this.months.mar;
          break;
        case 3:
          this.code = this.months.apr;
          break;
        case 4:
          this.code = this.months.may;
          break;
        case 5:
          this.code = this.months.june;
          break;
        case 6:
          this.code = this.months.july;
          break;
        case 7:
          this.code = this.months.aug;
          break;
        case 8:
          this.code = this.months.sept;
          break;
        case 9:
          this.code = this.months.oct;
          break;
        case 10:
          this.code = this.months.nov;
          break;
        case 11:
          this.code = this.months.dec;
          break;

        default:
          return "Error: More codes need adding";
          break;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.main_area {
  background-color: #7fd9c6;
  position: relative;
  padding: 30px 14px;
  width: 322px;
  border-radius: 20px;
  font-size: 0.9rem;
  letter-spacing: 1px;
  line-height: 1rem;
  -moz-box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
  -webkit-box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
  box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
}
.main_text_area {
  &_top_text {
    padding-inline: 10px;
    width: 100%;
    font-size: 12px;
  }
  &_middle_text {
    margin-top: 1.4rem;
    margin-left: auto;
    line-height: 14.5px;
    font-size: 12px;
  }
  &_bottom_text {
    margin-top: 0.8rem;
    margin-left: auto;
    line-height: 14.5px;
    font-size: 12px;
  }
}
.main_context {
  display: flex;
  flex-direction: row-reverse;
  &_text {
    width: 60%;
  }
}

.strong {
  font-weight: 700;

  &_and_underline {
    font-weight: 700;
    text-decoration: underline;
  }
}
.applogos {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.appstore img {
  width: 162px;
  margin-top: 2.4rem;
}

.googleplay img {
  width: 172px;
}

button {
  background-color: white;
  color: #7fd9c6;
  border: none;
  border-radius: 10px;
  padding: 15px 30px;
  width: 100%;
  font-size: 16px;
  z-index: 2;
  cursor: pointer;
  font-weight: 700;
  -moz-box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
  -webkit-box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
  box-shadow: 0px 0px 15px 0px rgba(51, 51, 51, 20%);
}

.code {
  color: white;
  margin-top: 1.2rem;
  font-size: 20px;
  text-align: center;
  line-height: 1.2;
  letter-spacing: 1.4px;
  padding: 0 20px;
}

.flashcharger_machine {
  position: absolute;
  top: 135px;
  left: -180px;
  z-index: 1;
}

.flashcharger_machine img {
  width: 300px;
}

.code_group {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 10px;
}

svg {
  width: 40px;
  padding-top: 20px;
}

@media (min-width: 800px) {
  .main_area {
    width: 600px;
    padding: 50px 100px;
  }

  .main_text_area {
    &_top_text {
      width: 100%;
      padding-inline: 0px;
      font-size: 18px;
      line-height: 24px;
    }
    &_middle_text,
    &_bottom_text {
      width: 100%;
      font-size: 18px;
      line-height: 24px;
    }
  }
  .main_context {
    display: flex;
    flex-direction: row-reverse;
    &_text {
      width: 100%;
    }
  }
  .applogos {
    flex-direction: row;
    align-items: center;
    justify-content: center;
    margin-top: 1.6rem;
    margin-right: 0;
  }
  .appstore img,
  .googleplay img {
    margin: 0 auto;
  }
  .appstore img {
    width: 200px;
  }
  .googleplay img {
    width: 218px;
    margin: 0;
  }

  .flashcharger_machine {
    position: absolute;
    top: 50px;
    left: -370px;
    z-index: 1;
  }

  .flashcharger_machine img {
    width: 450px;
  }

  svg {
    width: 40px;
  }

  .code {
    font-size: 24px;
  }
}

@media (min-width: 1280px) {
  .main_area {
    width: 750px;
    padding: 50px 100px;
  }

  .main_text_area {
    &_top_text {
      width: 100%;
      padding-inline: 0px;
      font-size: 20px;
      line-height: 24px;
    }
    &_middle_text,
    &_bottom_text {
      width: 100%;
      font-size: 20px;
      line-height: 24px;
    }
  }
  .main_context {
    display: flex;
    flex-direction: row-reverse;
    &_text {
      width: 100%;
    }
  }
  .applogos {
    flex-direction: row;
    align-items: center;
    justify-content: center;
    margin-top: 1.6rem;
    margin-right: 0;
  }
  .appstore img,
  .googleplay img {
    margin: 0 auto;
  }
  .appstore img {
    width: 200px;
  }
  .googleplay img {
    width: 218px;
    margin: 0;
  }

  .flashcharger_machine {
    position: absolute;
    top: 0px;
    left: -470px;
    z-index: 1;
  }

  .flashcharger_machine img {
    width: 540px;
  }

  .code {
    font-size: 30px;
  }
}
</style>
