<template>
      <nb-Container >
          <nb-tabs>
            <nb-tab heading="뉴스피드">
              <tab-one/>
            </nb-tab>
            <nb-tab heading="블루밍픽">
              <tab-two/>
            </nb-tab>
            <nb-tab heading="리서치">
              <tab-three/>
            </nb-tab>
            <nb-tab heading="포럼">
              <tab-four/>
            </nb-tab>
          </nb-tabs>
          <nb-Footer >
              <nb-FooterTab>
                  <nb-Button active >
                      <text>뉴스</text>
                      <nb-icon name="home"/>
                  </nb-Button>
                  <nb-Button>
                      <text>마켓</text>
                      <nb-Icon type="AntDesign" name="camera"/>
                  </nb-Button>
                  <nb-Button>
                      <text>멘토</text>
                      <nb-Icon name='ios-compass'  />
                  </nb-Button>
                  <nb-Button>
                      <text>더보기</text>
                      <nb-Icon type="AntDesign" name="contacts"  />
                  </nb-Button>
              </nb-FooterTab>
          </nb-Footer>
      </nb-Container>
</template>


<script>
import TabOne from "./components/tabOne";
import TabTwo from "./components/tabTwo";
import TabThree from "./components/tabThree";
import TabFour from "./components/tabFour";
import {Dimensions, ScrollView} from 'react-native'

export default {
  props: {
    navigation: {
      type: Object,
    }
  },
  data () {
    return {
      screenheight: 0,
    }
  },
  computed: {
    items () {
      return store.state.posts;
    },
    loading () {
        return store.state.loadingPosts;
    },
    wheight: () => {
      return Dimensions.get('window').height;
    },
  }, 
  created () {
  },
  methods: {

  },
  components: {
      TabOne,TabTwo,TabThree,TabFour
  }
}
</script>


<style>
</style>
