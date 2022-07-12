<template>
  <div class="comp-wrap">
    <button type="button" class="btn-normal small">normal</button>
    <button type="button" class="btn-normal2 small">normal2</button>
    <button type="button" class="btn-point small">point</button>
    <button type="button" class="btn-primary small">primary</button>
    <button type="button" class="btn-primary small disabled">primary</button>
    <br />
    <button type="button" class="btn-normal">normal</button>
    <button type="button" class="btn-normal2">normal2</button>
    <button type="button" class="btn-point">point</button>
    <button type="button" class="btn-primary">primary</button>
    <br />
    <button type="button" class="btn-normal large">normal</button>
    <button type="button" class="btn-normal2 large">normal2</button>
    <button type="button" class="btn-point large">point</button>
    <button type="button" class="btn-primary large">primary</button>
    <br /><br />
    <div class="btn-area type-row">
      <button type="button" class="btn-sns naver">네이버</button>
      <button type="button" class="btn-sns facebook">페이스북</button>
      <button type="button" class="btn-sns google">구글</button>
      <button type="button" class="btn-sns kakao">카카오</button>
      <button type="button" class="btn-sns apple">apple</button>
    </div>
    <br /><br />
    <div class="btn-area type-row">
      <button type="button" class="btn-sns naver icon">네이버</button>
      <button type="button" class="btn-sns facebook icon">페이스북</button>
      <button type="button" class="btn-sns google icon">구글</button>
      <button type="button" class="btn-sns kakao icon">카카오</button>
      <button type="button" class="btn-sns apple icon">apple</button>
    </div>
    <br />
    <br />
    <div class="btn-area">
      <button type="button" class="btn-normal">배송지 변경</button>
      <button type="button" class="btn-normal">변경신청 내역조회</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-row">
      <button type="button" class="btn-point">변경 신청 취소</button>
      <button type="button" class="btn-primary">변경신청 내역조회</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-row">
      <div class="row"><button type="button" class="btn-normal">normal</button><button type="button" class="btn-point wd90">변경 신청 취소</button></div>
      <div class="row"><button type="button" class="btn-primary">변경신청 내역조회</button></div>
    </div>
    <br />
    <br />
    type-bottom 페이지 하단에 fixed 되지 않고 들어가는 btn-area : margin-top:4rem
    <div class="btn-area type-bottom">
      <button type="button" class="btn-normal large fs13">normal-large : font-size:13px</button>
      <button type="button" class="btn-primary large">변경신청 내역조회</button>
    </div>
    <p class="txt-btn-assist">txt-btn-assist : 버튼 하단에 설명을 위한 text : margin-top:2rem;</p>
    <p class="txt-btn-assist narrow">txt-btn-assist + narrow : 버튼 하단에 설명을 위한 text : margin-top:1.5rem;</p>
    <br />
    <br />
    <div class="btn-area">
      <button type="button" class="btn-secondary x-large">장바구니 담기</button>
      <button type="button" class="btn-primary x-large">바로구매</button>
    </div>
    <br />
    <br />
    <div class="btn-area">
      <button type="button" class="btn-secondary x-large wp40">장바구니 담기</button>
      <button type="button" class="btn-primary x-large">바로구매</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-row">
      <button type="button" class="btn-primary large">수정 완료</button>
      <button type="button" class="btn-line fc-gray">기존 입력 값 유지</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-row">
      <div class="row"><button type="button" class="btn-point large">수정 완료</button><button type="button" class="btn-primary large">수정 완료</button></div>
      <div class="row"><button type="button" class="btn-line fc-gray">기존 입력 값 유지</button></div>
    </div>
    <br />
    <br />
    <div class="btn-area type-fixed">
      <button type="button" class="btn-secondary x-large">장바구니 담기</button>
      <button type="button" class="btn-primary x-large">바로구매</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-fixed">
      <button type="button" class="btn-secondary x-large wp40">장바구니 담기</button>
      <button type="button" class="btn-primary x-large">바로구매</button>
    </div>
    <br />
    <br />
    <div class="btn-area type-fixed type2">
      <button type="button" class="btn-secondary x-large">초기화</button>
      <button type="button" class="btn-primary x-large">리뷰 등록</button>
    </div>
    <br />
    <br />
    <button type="button" class="btn-arrow">내 배송지</button>
    <button type="button" class="btn-arrow green">내 배송지</button>
    <a href="#" class="btn-arrow gray">내 배송지</a>

    <a href="#" class="btn-arrow">내 배송지</a>

    <br /><br />
    <button type="button" class="btn-line">보기</button>
    <button type="button" class="btn-line fc-green">보기</button>
    <button type="button" class="btn-line fc-gray">보기</button>
    <br /><br />
    <button type="button" class="btn-text">보기</button>
    <button type="button" class="btn-text fc-green">보기</button>
    <button type="button" class="btn-text fc-gray">보기</button>
    <br /><br />
    <div class="sns-button">
      <a href="#none" class="google"><span class="hidden">구글로 회원가입</span></a>
      <a href="#none" class="kakao"><span class="hidden">카카오로 회원가입</span></a>
      <a href="#none" class="naver"><span class="hidden">네이버로 회원가입</span></a>
      <a href="#none" class="facebook"><span class="hidden">페이스북로 회원가입</span></a>
      <a href="#none" class="apple"><span class="hidden">Apple로 회원가입</span></a>
    </div>
    <br /><br />
    <div class="paging type-more">
      <button type="button">
        <span class="in">
          더보기<span class="num"><span class="current">10</span> / 999</span>
        </span>
      </button>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
      
  },
  layout: 'guide'
})
export default class HomePage extends Vue {
}
</script>
<style lang="scss">
</style>
