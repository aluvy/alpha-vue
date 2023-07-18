<template>

  <div class="container">
    <div class="content" id="content">
      <h2 class="title_nav">{{ layout.title }}</h2>

      <div class="section">
        <h3 class="tit02">중복된 이메일이 없을 경우</h3>
        <div class="btn_group">
          <button type="button" class="btn md c03" id="btn_loginPop03" @click="$popup.open('#loginPop03', '#btn_loginPop03');">Alert</button>
        </div>
      </div> <!-- // section -->

      <div class="section">
        <h3 class="tit02">기존 계정 또는 탈퇴한 경우</h3>
        <div class="btn_group">
          <button type="button" class="btn md c03" id="btn_loginPop04" @click="$popup.open('#loginPop04', '#btn_loginPop04');">Alert</button>
        </div>
      </div> <!-- // section -->

    </div> <!-- // content -->
  </div><!-- // container -->

</template>

<script>

export default {
  name: 'ALFM-LG04-PO00',
  emits: ['popupItem', 'setLayout'],
  data(){
    return {
      layout: { header: 'sub2', footer: '', title: '회원가입 메인 > 정보입력' },
      popupItem: ['loginPop03', 'loginPop04'],
    }
  },
  mounted(){
    this.$emit('setLayout', this.layout);
    this.$emit('popupItem', this.popupItem);
  }
}
</script>
