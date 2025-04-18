<template>
  <view class="pageview_content">
    <!-- 空状态-骨架屏 -->
    <view v-if="!isData" class="skeletonScreen">
      <!-- 小程序状态栏填充 -->
      <!-- #ifdef MP -->
      <!-- #ifndef MP-TOUTIAO -->
      <view :style="{ paddingTop: iStatusBarHeight + 'px' }"></view>
      <!-- #endif -->
      <!-- #endif -->
      <view class="search"> </view>
      <view class="tip">
        <view></view>
        <view></view>
        <view></view>
        <view></view>
      </view>
      <view class="banner">
        <view class="oBan">
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
        </view>
        <view class="tBan">
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
          <view class="oBlock">
            <view class="oBig"></view>
          </view>
        </view>
      </view>
      <view class="swiper sScreen">
        <view class="skeTitle"></view>
        <view class="sBeside">
          <view class="sBlock">
            <view></view>
          </view>
          <view class="sBlock">
            <view></view>
            <image
              src="https://cloudimage.qxdaojia.com/MALL/1696757080574_08667988177a396b03cc87a34b2f1f19.png"
              mode="scaleToFill"
              style="uc-perf-stat-ignore: image"
            />
          </view>
        </view>
      </view>
      <view class="events sScreen">
        <view class="skeTitle"></view>
        <view class="eOne"></view>
        <view class="eTwo">
          <view></view>
          <view></view>
        </view>
        <view class="eTwo">
          <view></view>
          <view></view>
        </view>
      </view>
      <view class="newGuest sScreen">
        <view class="skeTitle"></view>

        <view class="cont">
          <view class="block">
            <view class="top"></view>
          </view>
          <view class="block">
            <view class="top"></view>
          </view>
          <view class="block">
            <view class="top"></view>
          </view>
          <view class="block">
            <view class="top"></view>
          </view>
        </view>
      </view>
      <view class="discountZone">
        <view class="skeTitle"></view>
        <view class="cont">
          <view class="left"> </view>
          <view class="right">
            <view></view>
            <view style="margin-top: 16rpx"></view>
          </view>
        </view>
      </view>
    </view>
    <view v-else class="content">
      <image class="logo" src="/static/logo.png"></image>
      <view>
        <text class="title">{{ title }}</text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "Hello",
      isData: false,
    };
  },
  onLoad() {},
  methods: {},
};
</script>

<style scoped lang="scss">

//骨架屏
.skeletonScreen {
  background-color: #f6f6f6;
  padding-top: 12rpx;
  .search {
    width: 480rpx;
    height: 64rpx;
    margin-left: 20rpx;
    border-radius: 50rpx;
    background-color: #e2e3e5;
    padding: 17rpx 30rpx 0 0;
    image {
      width: 28rpx;
      height: 28rpx;
      float: right;
    }
  }
  .tip {
    width: 900rpx;
    display: flex;
    margin-left: 20rpx;
    padding: 29rpx 0 16rpx 0;
    view {
      width: 198rpx;
      height: 52rpx;
      border-radius: 40rpx;
      margin-right: 16rpx;
      background-color: #ffffff;
    }
  }
  .banner {
    background-color: #ffffff;
    padding: 16rpx 0 48rpx 24rpx;
    .oBan {
      display: flex;
      .oBlock {
        width: 176rpx;
      }
      .oBig {
        width: 126rpx;
        height: 126rpx;
        margin: 0 auto;
        border-radius: 24rpx;
        background: #f2f2f2;
        margin-bottom: 8rpx;
      }
      .oSmall {
        width: 112rpx;
        height: 28rpx;
        margin: 0 auto;
        border-radius: 8rpx;
        background: #f2f2f2;
      }
    }
    .tBan {
      display: flex;
      margin-top: 24rpx;
      .oBlock {
        width: 142rpx;
      }
      .oBig {
        width: 110rpx;
        height: 110rpx;
        margin: 0 auto;
        border-radius: 24rpx;
        background: #f2f2f2;
        margin-bottom: 8rpx;
      }
      .oSmall {
        width: 104rpx;
        height: 26rpx;
        margin: 0 auto;
        border-radius: 8rpx;
        background: #f2f2f2;
      }
    }
  }
  .skeTitle {
    width: 144rpx;
    height: 34rpx;
    border-radius: 8rpx;
    background-color: #f1f1f1;
    //  @include text(36rpx, 550, #333);
    padding-left: 4rpx;
  }
  .sScreen {
    background-color: #ffffff;
    border-radius: 16rpx;
    margin: 16rpx;
    padding: 30rpx 16rpx 16rpx 16rpx;
  }
  .swiper {
    overflow: hidden;
    .sBeside {
      display: flex;
      width: 1400rpx;
    }
    .sBlock {
      width: 640rpx;
      height: 320rpx;
      border-radius: 24rpx;
      background-color: #e2e3e5;
      margin-top: 26rpx;
      margin-right: 16rpx;
      // view{
      // 	height: 320rpx;
      // 	border-radius: 24rpx;
      // 	background-color: #E2E3E5;
      // }
      image {
        width: 55rpx;
        height: 62rpx;
        float: right;
      }
    }
  }
  .events {
    .eOne {
      width: 686rpx;
      height: 200rpx;
      border-radius: 24rpx;
      background: #f1f1f1;
      margin-top: 26rpx;
    }
    .eTwo {
      display: flex;
      justify-content: space-between;
      margin-top: 16rpx;
      view {
        border-radius: 24rpx;
        background: #f1f1f1;
        width: 334rpx;
        height: 128rpx;
      }
    }
  }
  .newGuest {
    position: relative;
    overflow: hidden;
    .check {
      display: flex;
      align-items: center;
      position: absolute;
      top: 38rpx;
      right: 20rpx;
      text {
        @include text(28rpx, 400, #666);
      }
      image {
        width: 24rpx;
        height: 24rpx;
      }
    }
    .cont {
      display: flex;
      margin-top: 28rpx;
      .block {
        margin-right: 16rpx;
        .top {
          width: 186rpx;
          height: 186rpx;
          border-radius: 16rpx;
          background: linear-gradient(0deg, #e2e3e5 0%, #e2e3e5 100%),
            lightgray 50% / cover no-repeat;
        }
        .midd {
          width: 188rpx;
          height: 40rpx;
          border-radius: 16rpx;
          background: #f1f1f1;
          margin: 14rpx 0;
        }
        .bottom {
          width: 116rpx;
          height: 24rpx;
          border-radius: 16rpx;
          background: #f1f1f1;
        }
      }
    }
  }
  .discountZone {
    margin: 32rpx 0 0 20rpx;
    padding-bottom: 40rpx;
    .cont {
      display: flex;
      padding-top: 10rpx;
      .left {
        width: 348rpx;
        height: 306rpx;
        border-radius: 16rpx;
        background: #e2e3e5;
        margin-right: 18rpx;
        view {
          height: 50rpx;
          width: 140rpx;
          border-radius: 18px;
          background: #fff;
          margin-top: 230rpx;
          margin-left: 24rpx;
        }
      }
      .right {
        view {
          width: 346rpx;
          height: 144rpx;
          border-radius: 16rpx;
          background: #e2e3e5;
        }
      }
    }
  }
}
.skeletonScreen::after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  z-index: 9;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    100deg,
    rgba(255, 255, 255, 0) 50%,
    rgba(255, 255, 255, 0.5) 55%,
    rgba(255, 255, 255, 0) 60%
  );
  background-size: 200% 100%;
  background-position-x: 180%;
  animation: 1.5s loading ease-in-out infinite;
}
@keyframes loading {
  to {
    background-position-x: -20%;
  }
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin: 200rpx auto 50rpx auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
