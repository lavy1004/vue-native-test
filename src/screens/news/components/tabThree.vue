<template>
  <nb-container>
    <nb-content padder>
      <nb-h1 class="mt10">베스트 뉴스</nb-h1>
      <nb-card>
        <nb-card-item cardBody>
            <nb-left  class="card-item-image">
              <image :source="cardImage" class="w100" :style="stylesObj.cardItemImage"/>
            </nb-left>
            <nb-right>
                <nb-text>갤럭시 S10 '삼성 블록체인 월렛'에 트론 디앱 3종 추가</nb-text>
                <nb-text>트론 기반 디앱들이 삼성전자 갤럭시 S10의 '삼성 블록체인 월렛'에 새로 탑재됐다. 삼성 블록체인 월렛은 암호화폐 송금 등 지갑 기능과 디앱을 바로 접속할 수 있는 앱이다.</nb-text>
            </nb-right>
        </nb-card-item>
        <nb-card-item>
          <nb-left>
            <nb-button transparent>
              <nb-icon name="happy" active></nb-icon>
              <nb-text>60%</nb-text>
            </nb-button>
          </nb-left>
          <nb-body>
            <nb-button transparent>
              <nb-text>추천 +20</nb-text>
            </nb-button>
          </nb-body>
          <nb-right>
            <nb-icon name="bookmark" active></nb-icon>
            <nb-text>5</nb-text>
          </nb-right>
        </nb-card-item>
      </nb-card>

      <view >
        <nb-h1 class="mt10">뉴스 피드</nb-h1>
        <nb-text>오늘 2019년 12월 23일 월요일</nb-text>
        <nb-view class="flex-group">
          <nb-text class="time">17:37</nb-text>
          <nb-text class="feed">KISA, 한국거래소 기술특례상장 전문평가기관 지정... 핀테크.블록체인.융합보안 전문평가 한국인터넷 진흥원은 유망기술력을 갖춘 스타트업이 이익실현...</nb-text>
        </nb-view>
        <nb-view class="flex-group">
          <nb-text class="time">17:37</nb-text>
          <nb-text class="feed">KISA, 한국거래소 기술특례상장 전문평가기관 지정... 핀테크.블록체인.융합보안 전문평가 한국인터넷 진흥원은 유망기술력을 갖춘 스타트업이 이익실현...</nb-text>
        </nb-view>
        <nb-view class="flex-group">
          <nb-text class="time">17:37</nb-text>
          <nb-text class="feed">KISA, 한국거래소 기술특례상장 전문평가기관 지정... 핀테크.블록체인.융합보안 전문평가 한국인터넷 진흥원은 유망기술력을 갖춘 스타트업이 이익실현...</nb-text>
        </nb-view>
        <nb-view class="flex-group">
          <nb-text class="time danger">17:37</nb-text>
          <nb-text class="feed danger-c">12월 24일 블루밍비트 정오시황</nb-text>
        </nb-view>
      </view>
      
    </nb-content>
    
  </nb-container>
</template>

<script>

  import cardImage from "./drawer-cover.jpg";

  export default {
     props: {
       
    },
    mounted() {
     
    },
    data: function() {
      return {
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
  flex: 0.5;
  height: 100%;
}

.flex-group{
  display: flex;
  flex-direction: row;
  padding-top:10px;
}
.time{
  flex:2;
  text-align:center;
  border-radius:5;
  background-color: #eee;
  height:100%;
}
.feed{
  margin-left: 10px;
  flex:8
}

.danger {
  background-color: crimson
}

.danger-c {
  color: crimson
}

.w100{
  width:100%;
  height:100%;
}

.mt10{
  margin-top: 10px;
}

</style>