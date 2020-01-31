<template>
  <nb-container>
    <nb-header>
      <nb-left>
        <nb-button transparent :onPress="() => user.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>프로필</nb-title>
      </nb-body>
    </nb-header>
    <nb-content padder>
      <nb-card>
        <nb-card-item>
          <nb-left>
            <nb-thumbnail :source="{uri:logo}"></nb-thumbnail>
            <nb-body>
              <nb-text>NativeBase</nb-text>
              <nb-text note>{{user.state.params.id}}</nb-text>
            </nb-body>
          </nb-left>
        </nb-card-item> 
        <nb-card-item cardBody>
            <image :source="cardImage" class="card-item-image" :style="stylesObj.cardItemImage"/>
        </nb-card-item>
        <nb-card-item>
          <nb-left>
            <nb-button transparent>
              <nb-icon name="thumbs-up" active></nb-icon>
              <nb-text>4923 Likes</nb-text>
            </nb-button>
          </nb-left>
          <nb-body>
            <nb-button transparent>
              <nb-icon name="chatbubbles" active></nb-icon>
              <nb-text>Comment</nb-text>
            </nb-button>
          </nb-body>
          <nb-right>
            <nb-text>11h ago</nb-text>
          </nb-right>
        </nb-card-item>
      </nb-card>
      <view class="test2">
        <text class="test1">
          안녕하세요
        </text>
        <text class="test3">
          안녕하세요222
        </text>
      </view>
    </nb-content>
    
  </nb-container>
</template>
<script>
  import cardImage from "./drawer-cover.jpg";
  export default {
     props: {
        user: {
        type: Object,
        }
    },
    mounted() {
      this.logo = this.user.state.params.img
      console.log(this.user.state.params.img)
    },
    data: function() {
      return {
        logo:'https://s3.amazonaws.com/uifaces/faces/twitter/bigmancho/128.jpg',
        cardImage,
        stylesObj: {
          cardItemImage: {
            resizeMode: "cover"
          }
        }
      };
    }
  };
</script>
<style>
  .card-item-image {
    flex: 1;
    height: 500;
  }
  .test2{
    position: relative;
    width: 100%;
    height: 400;
    background-color: red;
  }
  .test1{
    position: absolute;
    top:0;
    width: 100%;
    height: 200;
    background-color:aqua;
  }
  
  .test3{
    position: absolute;
    top:0;
    height: 200;
    background-color:gold;
  }
</style>