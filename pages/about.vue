<template lang="pug">
.about-container
  CustomTransition
  .section.profile
    .title Profile
    .profile-container
      .icon
      .bio
        .name しろねぎ
        .skills
          .do Do <span>Pixelart 動画編集</span>
          .like Like <span>Webdesign Illustration</span>
          .interest Interest <span>Live2D AR ゲーム制作 3DCG</span>
  .section.achievement
    .title Achievement
    .achievement-container
      .item
        .thumbnail
        .text 動画編集 よりぬき
      .item
        .thumbnail
        .text ドット絵 配信ED
      .item
        .thumbnail
        .text イラスト 配信背景
      .item
        .thumbnail
        .text webアプリ マジカルミライ10th Anniversary
  .section.links Links

</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  name: 'AboutPage'
})
</script>

<style scoped lang="scss">
@import "~/assets/sass/app";

.about-container {
  font-size: 4vw;
}

.section {
  padding: 2vw;
}

.profile {
  // padding: 2vw;

  .title {
    width: 100%;
  }

  .profile-container {
    display: flex;
    justify-content: space-around;

    .icon {
      background-color: $theme-color;
    }

    .bio {
      display: grid;

      .name {
        font-size: 8vw;
      }

      .skills {
        span {
          margin-left: 2vw;
        }

        .do {
          font-size: 3vw;
        }

        .like {
          font-size: 2.2vw;
        }

        .interest {
          font-size: 1.3vw;
        }
      }
    }
  }
}

.achievement {
  .title {
    width: 100%;
  }

  .achievement-container {
    display: flex;
    flex-direction: column;
    justify-content: space-around;

    .item {
      display: flex;

      .thumbnail {
        width: 20vw;
        background-color: $theme-color;
      }

      .text {
        width: 70vw;
        font-size: 2vw;
      }
    }
  }
}

@include pc {
  .profile-container {
    flex-direction: row;

    .icon {
      width: 33vw;
      height: 33vw;
    }

    .bio {
      width: 50vw;
    }
  }
}

@include smartphone {
  .profile-container {
    flex-direction: column;

    .icon {
      width: 80vw;
      height: 80vw;
    }

    .bio {
      width: 80vw;
    }
  }
}

</style>
