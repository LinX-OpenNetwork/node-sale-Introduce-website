<script setup lang="ts">
const featureArray: any = [
  {
    iconName: 'guardian',
    title: 'Guardian',
    content: `Guardian play the role of a police officer, responsible for judging the quality of the Edge Node's work.`
  },
  {
    iconName: 'watchDog',
    title: 'WatchDog',
    content: 'Watch Dog plays the role of a security guard who, along with Guardian, is responsible for verifying that the Edge Node is working correctly in the network.'
  },
  {
    iconName: 'nodeFlow',
    title: 'EdgeNode',
    content: 'The Edge Node acts as a messenger, transmitting, relaying, and routing messages.'
  },
]
</script>

<template>
  <div class="part_three">
    <div class="part_three_title">
      <h1>
        How does our <br class="mobile" />platform work ?
      </h1>
      <p>
        The SendingNetwork integrates three essential roles for its operation: Container, Indexer, and Checker.
      </p>
    </div>

    <div class="part_three_detail">

      <div class="part_three_features">
        <template v-for="(item, i) of featureArray" :key="i">
          <div class="part_three_feature_item">
            <SdkIcon :name="item.iconName" size="2.5rem" />
            <div class="part_three_feature_introduce">
              <h3>{{ item.title }}</h3>
              <p>{{ item.content }}</p>
            </div>
          </div>
        </template>
      </div>

      <div class="part_three_card">
        <h2>
          Join WatchDog<br/>Node Sale
        </h2>
        <p>
          Be a part of the largest node sale and help shape the future of AI and gaming. Get ready to power up the cloud
          with SendingNetwork!
        </p>
        <a href="">
          <SdkButton style="background: #38CA9F;">Purchase a WatchDog Licence (NFT)</SdkButton>
        </a>
        <div class="footer" />
      </div>

    </div>

  </div>
</template>

<style scoped>
.part_three {
  color: white;
  padding: 0 1.3889rem;
  p{
    color: #EAFAF0;
    opacity: 0.75;
  }

  .part_three_title {
    padding-bottom: .9259rem;
    h1, p{
      text-align: center;
    }
    h1 {
      font-size: 1.4815rem;
    }
    p{
      font-size: .3704rem;
    }
  }

  .part_three_detail{
    display: flex;
    align-items: center;
    padding-bottom: .7407rem;

    height: 12.2222rem;
    .part_three_features{
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      .part_three_feature_item{
        display: flex;
        .part_three_feature_introduce{
          margin-left: .7704rem;
          h3{
            color: #38CA9F;
            font-size: .7407rem;
            font-weight: 600;
            line-height: 130%;
            letter-spacing: -0.0148rem;
          }
          p{
            font-size: .2963rem;
            line-height: 140%; /* 22.4px */
          }
        }
      }
    }
    .part_three_card{
      position: relative;
      border: 1px solid #3e4040;
      border-radius: .3704rem;
      margin-left: .9259rem;
      height: 100%;
      h2{
        margin:.7407rem .3704rem;
        font-size: .5926rem;
        font-weight: 600;
        line-height: 130%;
        letter-spacing: -0.0119rem;
      }
      p{
        margin:.7407rem .3704rem;
        opacity: 0.72;
        font-size: .2963rem;
        font-weight: 600;
        line-height: 140%;
      }
      a{
        width: 100%;
        display: flex;
        justify-content: center;
      }
      .footer{
        z-index: -1;
        position: absolute;
        left: 0;
        bottom: 0;
        height: 6.1111rem;
        width: 100%;
        background: url('@/assets/imgs/part_three_card.png');
        background-size:100%  100% ;
        background-position: center;
        background-repeat: no-repeat;

      }
    }
  }

}

@media screen and (max-width: 999.999px) {
.part_three {
  color: white;
  padding: 0 .4444rem;
  .part_three_title {
    h1, p{
      text-align: center;
    }
    h1 {
      font-size: .6667rem;
      text-align: start;
    }
    p{
      font-size: .2963rem;
      text-align: start;
      opacity: 0.72;
    }
  }

  .part_three_detail{
    padding-bottom: .7407rem;
    flex-direction: column;
    height: 23.1481rem;

    .part_three_features{
      .part_three_feature_item{
        .part_three_feature_introduce{
          h3{
            font-size: .5926rem;
          }
        }
      }
    }
    .part_three_card{
      margin-top: .3704rem;
      margin-left: 0;
      .footer{
        margin-top: .3704rem;
        background-position: bottom;
      }
    }
  }

}

}</style>