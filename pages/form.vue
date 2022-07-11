<template>
  <div class="comp-wrap">
    inp:radio, checkbox 요소들은 inp가 기본값입니다.<br />
    <span class="inp" v-for="(item, index) in radioList1" :key="'radio1-' + index">
      <input type="radio" :id="'radio1-' + index" name="radio1" v-model="radio1" :value="item.value" /><label :for="'radio1-' + index"
        ><span class="ftext">{{ item.value }}</span></label
      >
    </span>
    선택된 값 : {{ radio1 }} <br /><br />
    inp요소들이 한줄로 균등하게 배열될 때는 form-area로 감쌉니다.
    <div class="form-area">
      <span class="inp" v-for="(item, index) in radioList2" :key="'radio2-' + index">
        <input type="radio" :id="'radio2-' + index" name="radio2" v-model="radio2" :value="item.value" /><label :for="'radio2-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    inp요소들이 텍스트의 길이에 따라 여러줄이 될 가능성이 있을때는 form-area + flex를 이용합니다
    <div class="form-area flex">
      <span class="inp" v-for="(item, index) in radioList6" :key="'radio6-' + index">
        <input type="radio" :id="'radio6-' + index" name="radio6" v-model="radio6" :value="item.value" /><label :for="'radio6-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    inp요소들'만' 있을 시 한줄에 2개, 한줄에 3개... 이런식으로 등분되어 나오게되면 grid2, grid3... 을 넣어줍니다.
    <div class="form-area grid2">
      <span class="inp" v-for="(item, index) in radioList3" :key="'radio3-' + index">
        <input type="radio" :id="'radio3-' + index" name="radio3" v-model="radio3" :value="item.value" /><label :for="'radio3-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    <span class="inp" v-for="(item, index) in checkboxList1" :key="'checkbox1-' + index">
      <input type="checkbox" :id="'checkbox1-' + index" v-model="checkbox1" :value="item.value" /><label :for="'checkbox1-' + index"
        ><span class="ftext">{{ item.value }}</span></label
      >
    </span>
    선택된 값 : {{ checkbox1 }} <br /><br />
    <div class="form-area">
      <span class="inp" v-for="(item, index) in checkboxList2" :key="'checkbox2-' + index">
        <input type="checkbox" :id="'checkbox2-' + index" v-model="checkbox2" :value="item.value" /><label :for="'checkbox2-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    <div class="form-area grid2">
      <span class="inp" v-for="(item, index) in checkboxList3" :key="'checkbox3-' + index">
        <input type="checkbox" :id="'checkbox3-' + index" v-model="checkbox3" /><label :for="'checkbox3-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    <div class="sq-area">
      <span class="inp-sq" v-for="(item, index) in radioList1" :key="'radio1-' + index">
        <input type="radio" :id="'radio1-' + index" name="radio1" v-model="radio1" :value="item.value" /><label :for="'radio1-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    일반
    <div class="sq-area">
      <span class="inp-sq" v-for="(item, index) in checkboxList3" :key="'checkbox3-' + index">
        <input type="checkbox" :id="'checkbox3-' + index" v-model="checkbox3" :value="item.value" /><label :for="'checkbox3-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    line형
    <div class="sq-area">
      <span class="inp-sq line" v-for="(item, index) in radioList1" :key="'radio1-' + index">
        <input type="radio" :id="'radio1-' + index" name="radio1" v-model="radio1" :value="item.value" /><label :for="'radio1-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    <div class="sq-area day">
      <span class="inp-sq" v-for="(item, index) in checkboxDayList" :key="'checkboxDay-' + index">
        <input type="checkbox" :id="'checkboxDay-' + index" v-model="checkboxDay" :value="item.value" :disabled="item.disabled" /><label :for="'checkboxDay-' + index"
          ><span class="ftext">{{ item.value }}</span></label
        >
      </span>
    </div>
    <br /><br />
    inp-box : checkbox와 radio가 vertical 중앙으로 오게 하려면 vc 클래스를 사용합니다.
    <div class="inp-box vc" v-for="(item, index) in checkboxList4" :key="'checkbox4-' + index">
      <input type="checkbox" :id="'checkbox4-' + index" v-model="checkbox4" :value="item.value" /><label :for="'checkbox4-' + index"><span v-html="item.value"></span></label>
    </div>
    <div class="inp-box" v-for="(item, index) in radioList5" :key="'radio5-' + index">
      <input type="radio" :id="'radio5-' + index" name="radio1" v-model="radio5" :value="item.value" /><label :for="'radio5-' + index"
        ><span>{{ item.value }}</span></label
      >
    </div>
    <br /><br />
    <span class="sel">
      <select v-model="select1">
        <option value="none">선택</option>
        <option v-for="(item, index) in selectList1" :key="index" :value="item.value">{{ item.value }}</option>
      </select>
    </span>
    <span class="sel bold">
      <select v-model="select1">
        <option value="none">bold</option>
        <option v-for="(item, index) in selectList1" :key="index" :value="item.value">{{ item.value }}</option>
      </select>
    </span>
    <span class="sel small">
      <select v-model="select1">
        <option value="none">small</option>
        <option v-for="(item, index) in selectList1" :key="index" :value="item.value">{{ item.value }}</option>
      </select>
    </span>
    select 선택된 값 : {{ select1 }} <br /><br />
    form-area안에 쓰이는 요소들은 기본적으로 등분 되고, 요소가 1개일때는 full로 꽉차게 됩니다.
    <div class="form-area">
      <span class="sel">
        <select v-model="select2">
          <option value="none">선택</option>
          <option v-for="(item, index) in selectList2" :key="index" :value="item.value">{{ item.value }}</option>
        </select>
      </span>
    </div>
    <br />
    <div class="form-area">
      <span class="sel">
        <select v-model="select2" class="disabled" disabled>
          <option value="none">선택</option>
          <option v-for="(item, index) in selectList2" :key="index" :value="item.value">{{ item.value }}</option>
        </select>
      </span>
    </div>
    <br /><br />
    <div class="dropdown type-sel" :class="dropdown ? 'on' : ''">
      <button type="button" @click="dropdownToggle" class="btn-drop">
        <template v-if="dropdownSelected == ''">type-sel</template><span class="selected-option" v-else>{{ dropdownSelected }}</span>
      </button>
      <ul class="option-drop">
        <li v-for="(item, index) in dropdownList" :key="index">
          <button type="button" @click="selected(index)" :class="{ selected: item.selected }">{{ item.option }}</button>
        </li>
      </ul>
    </div>
    <div class="dropdown type-sort" :class="dropdown ? 'on' : ''">
      <button type="button" @click="dropdownToggle" class="btn-drop">
        <template v-if="dropdownSelected == ''">type-sel</template><span class="selected-option" v-else>{{ dropdownSelected }}</span>
      </button>
      <ul class="option-drop">
        <li v-for="(item, index) in dropdownList" :key="index">
          <button type="button" @click="selected(index)" :class="{ selected: item.selected }">{{ item.option }}</button>
        </li>
      </ul>
    </div>
    <br /><br />
    form-area > 요소가 여러가지인 경우(균등비율로 배분)
    <div class="form-area">
      <span class="sel">
        <select v-model="select3">
          <option value="none">선택</option>
          <option v-for="(item, index) in selectList3" :key="index" :value="item.value">{{ item.value }}</option>
        </select>
      </span>
      <button type="button" class="btn-point large">선택</button>
      <button type="button" class="btn-normal large">선택</button>
    </div>
    <br /><br />
    form-area 안의 요소들이 1줄이고 균등으로 배분되지 않을 경우 > 정확한 값을 가지는 요소에게 wd..(ex:wd90 - width:90px, wp90 - width:90%) 클래스를 넣어줍니다.
    <div class="form-area">
      <span class="sel">
        <select v-model="select4">
          <option value="none">선택</option>
          <option v-for="(item, index) in selectList4" :key="index" :value="item.value">{{ item.value }}</option>
        </select>
      </span>
      <button type="button" class="btn-point large wd90">선택</button>
    </div>

    <br /><br />
    form-area 안의 요소들이 여러 줄인 경우 type-row클래스를 넣어주고, 각 줄을 div.row로 감쌉니다.
    <div class="form-area type-row">
      <div class="row">
        <span class="sel">
          <select v-model="select5">
            <option value="none">선택</option>
            <option v-for="(item, index) in selectList5" :key="index" :value="item.value">{{ item.value }}</option>
          </select>
        </span>
        <button type="button" class="btn-point large">선택</button>
      </div>
      <div class="row">
        <span class="sel">
          <select v-model="select6">
            <option value="none">선택</option>
            <option v-for="(item, index) in selectList6" :key="index" :value="item.value">{{ item.value }}</option>
          </select>
        </span>
        <button type="button" class="btn-point large wd90">선택</button>
      </div>
      <div class="row">
        <input type="text" class="tf" value="input" />
        <button type="button" class="btn-point large wd90">등록</button>
      </div>
      <div class="row"><button type="button" class="btn-normal large">선택</button></div>
    </div>
    <br /><br />
    <b-numberinput :editable="false" min="1" v-model="numberinput" class="inp-num"></b-numberinput>
    <b-numberinput :editable="false" min="1" v-model="numberinput" class="inp-num small"></b-numberinput>
    <br /><br />
    <input type="text" class="tf" placeholder="input" />
    <br /><br />
    <span class="tf-search">
      <input type="text" class="tf" placeholder="input" />
      <button type="button" class="btn-search"><span class="hidden">검색</span></button>
    </span>
    <br /><br />
    <textarea class="tfarea" cols="30" rows="10" placeholder="예) 레시피카드가 더 상세하게 나왔으면 좋겠어요!" />
    <br /><br />
    <div class="tfarea-box">
      <textarea class="tfarea" cols="30" rows="5" maxlength="80" v-model="tfareaWords" placeholder="메시지를 입력해 주세요." />
      <span class="words"
        ><span class="num">{{ tfareaWords.length }}</span> / 80</span
      >
    </div>
    <br /><br />
    form-item은 form-tit과 form-cont로 구성되며, 여러개의 form-item이 사용될 경우 div.list-form-area로 감싼다<br />
    list-form-area + type-narrow : 기본 여백 3rem이 아닌 2rem일 때 사용한다.
    <div class="form-item">
      <div class="form-tit">
        <strong class="tit"
          >신용카드<span class="required"><span class="hidden">필수입력</span></span></strong
        >
      </div>
      <div class="form-cont">
        <div class="form-area">
          <input type="number" class="tf center" maxlength="4" />
          <input type="number" class="tf center" maxlength="4" />
          <input type="number" class="tf center" maxlength="4" />
          <input type="number" class="tf center" maxlength="4" />
        </div>
      </div>
    </div>
    <br /><br />
    form-item + col
    <div class="form-item col">
      <div class="form-tit">
        <strong class="tit"
          >이름<span class="required"><span class="hidden">필수입력</span></span></strong
        >
      </div>
      <div class="form-cont">
        <input type="text" class="tf" placeholder="내용 입력" />
      </div>
    </div>
    <br /><br />
    list-form-area
    <div class="list-form-area">
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">카드번호</strong>
        </div>
        <div class="form-cont">
          <div class="form-area type-row">
            <div class="row">
              <input :type="checkboxCardNum ? 'number' : 'password'" class="tf center" :class="checkboxCardNum ? '' : 'disabled'" maxlength="4" />
              <input :type="checkboxCardNum ? 'number' : 'password'" class="tf center" :class="checkboxCardNum ? '' : 'disabled'" maxlength="4" />
              <input :type="checkboxCardNum ? 'number' : 'password'" class="tf center" :class="checkboxCardNum ? '' : 'disabled'" maxlength="4" />
              <input :type="checkboxCardNum ? 'number' : 'password'" class="tf center" :class="checkboxCardNum ? '' : 'disabled'" maxlength="4" />
            </div>
            <div class="row">
              <span class="inp">
                <input type="checkbox" id="checkboxCardNum" v-model="checkboxCardNum" /><label for="checkboxCardNum"><span class="ftext">카드 번호 보이게</span></label>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">유효기간</strong>
        </div>
        <div class="form-cont">
          <div class="tf-valid">
            <input type="number" class="tf center disabled" placeholder="MM" title="유효기간 월" />
            <span class="unit">/</span>
            <input type="number" class="tf center disabled" placeholder="YY" title="유효기간 년" />
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >배송지명<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <input type="text" class="tf" placeholder="내용 입력" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >받으시는 분<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <input type="text" class="tf" placeholder="내용 입력" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >연락처<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <div class="form-area">
            <span class="sel">
              <select v-model="selCall">
                <option value="none">선택</option>
                <option v-for="(item, index) in selectCallList" :key="index" :value="item.value">{{ item.value }}</option>
              </select>
            </span>
            <input type="number" class="tf center" />
            <input type="number" class="tf center" />
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >휴대폰번호<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <div class="form-area type-row">
            <div class="row">
              <span class="sel">
                <select v-model="selPhone">
                  <option value="none">선택</option>
                  <option v-for="(item, index) in selectPhoneList" :key="index" :value="item.value">{{ item.value }}</option>
                </select>
              </span>
              <input type="number" class="tf center" />
              <input type="number" class="tf center" />
            </div>
            <div class="row"><button type="button" class="btn-primary large">인증번호 요청</button></div>
            <div class="row">
              <input type="text" value="input" class="tf" />
              <button type="button" class="btn-point large wd90">인증번호 확인</button>
            </div>
            <ul class="txt-assist type-reference">
              <li>휴대폰번호 변경시 재인증 필수입니다.</li>
              <li>인증번호 발송은 통신사 사정에 따라 다소 지연될 수 있습니다.</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >주소<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <div class="form-area type-address">
            <div class="row">
              <input type="text" class="tf disabled" readonly value="" />
              <button type="button" class="btn-point large wd90">우편번호 찾기</button>
            </div>
            <div class="row">
              <input type="text" class="tf disabled" readonly placeholder="주소" value="" />
            </div>
            <div class="row">
              <input type="text" class="tf" placeholder="상세 주소" value="" />
            </div>
            <div class="row">
              <span class="inp">
                <input type="checkbox" id="basicAddress" value="기본 배송지로 저장" /><label for="basicAddress"><span class="ftext">기본 배송지로 저장</span></label>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">이메일</strong>
        </div>
        <div class="form-cont">
          <div class="form-area type-email">
            <div class="row">
              <input type="text" class="tf" value="gildong" />
              <span class="unit">@</span>
              <input type="text" class="tf" :value="selEmail == 'none' ? '' : selEmail" :readonly="selEmail == 'none' ? 'readonly' : ''" />
            </div>
            <div class="row">
              <span class="sel">
                <select v-model="selEmail">
                  <option value="none">직접 입력</option>
                  <option v-for="(item, index) in selEmailList" :key="index" :value="item.value">{{ item.value }}</option>
                </select>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">휴대전화번호, 이메일</strong>
        </div>
        <div class="form-cont">
          <span class="inp" v-for="(item, index) in radioList4" :key="'radio4-' + index">
            <input type="radio" :id="'radio4-' + index" name="radio4" v-model="radio4" :value="item.value" /><label :for="'radio4-' + index"
              ><span class="ftext">{{ item.value }}</span></label
            >
          </span>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >주문자 정보<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <div class="form-area">
            <input type="text" class="tf wp43" value="홍길동" />
            <input type="text" class="tf disabled" disabled value="010-9217-5545" />
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >배송요청 시간<span class="required"><span class="hidden">필수입력</span></span></strong
          >
        </div>
        <div class="form-cont">
          <div class="form-area">
            <span class="sel">
              <select v-model="selDeliveryTime">
                <option value="none">배송 시간을 선택해 주세요</option>
                <option v-for="(item, index) in selDeliveryTimeList" :key="index" :value="item.value">{{ item.value }}</option>
              </select>
            </span>
            <div class="txt-assist x-small">배송시간은 당일 전달 상황에 따라 다소 변동이 있을 수 있습니다.</div>
            <div class="txt-assist type-reference">배송지마다 배송 가능 요일은 다를 수 있음</div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">배송요청 사항</strong>
        </div>
        <div class="form-cont">
          <div class="form-area type-row">
            <div class="row">
              <span class="sel">
                <select v-model="selDeliveryAsk">
                  <option value="none">선택</option>
                  <option v-for="(item, index) in selDeliveryAskList" :key="index" :value="item.value">{{ item.value }}</option>
                </select>
              </span>
            </div>
            <div class="row">
              <textarea class="tfarea" cols="30" rows="5" placeholder="배송 요청 사항을 입력해주세요." />
            </div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">직구 (3)</strong>
        </div>
        <div class="form-cont">
          <div class="sq-area">
            <span class="inp-sq" v-for="(item, index) in checkboxList3" :key="'checkbox3-' + index">
              <input type="checkbox" :id="'checkbox3-' + index" v-model="checkbox3" :value="item.value" /><label :for="'checkbox3-' + index"
                ><span class="ftext">{{ item.value }}</span></label
              >
            </span>
          </div>
          <div class="txt-assist danger">성별을 선택해주세요.</div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">생년월일</strong>
        </div>
        <div class="form-cont">
          <div class="tf-ymd">
            <input type="number" maxlength="4" minlength="4" placeholder="0000" value="9999" title="태어난 년도" />년
            <input type="number" maxlength="2" minlength="2" placeholder="00" value="99" title="태어난 월" />월
            <input type="number" maxlength="2" minlength="2" placeholder="00" value="99" title="태어난 일" />일
          </div>
          <div class="txt-assist fc-red">생년월일을 입력해주세요.</div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">마지막 월경일 / 주기</strong>
        </div>
        <div class="form-cont">
          <div class="tf-ymd">
            <input type="number" maxlength="4" minlength="4" placeholder="0000" value="9999" title="마지막 월경일 년도" />년
            <input type="number" maxlength="2" minlength="2" placeholder="00" value="99" title="마지막 월경 월" />월
            <input type="number" maxlength="2" minlength="2" placeholder="00" value="99" title="마지막 월경 일" />일
            <span class="unit">/</span>
            <input type="number" maxlength="2" minlength="2" placeholder="00" value="99" title="월경 주기" />일
          </div>
          <div class="txt-assist fc-red">마지막 월경일 / 주기를 입력해주세요.</div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">비밀번호</strong>
        </div>
        <div class="form-cont">
          <input type="password" placeholder="비밀번호를 입력해주세요" class="tf" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">비밀번호</strong>
        </div>
        <div class="form-cont">
          <div class="form-area">
            <span class="card-type">
              <input type="password" placeholder="앞2자리" class="tf" />
              <span class="type">비씨</span>
            </span>
            <button type="button" class="btn-point large wd90">유효성 체크</button>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">비밀번호</strong>
        </div>
        <div class="form-cont">
          <div class="tf-mask">
            <input :type="toggleMask ? 'password' : 'text'" placeholder="비밀번호를 입력해주세요" class="tf" value="1234" />
            <button type="button" class="btn-mask" @click="toggleMask = !toggleMask" :class="toggleMask ? '' : 'on'"><span class="hidden">숨겨진 필드 표시</span></button>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">선물메세지</strong>
          <span class="append"
            ><span class="words">{{ tfareaWords.length }} / 300</span></span
          >
        </div>
        <div class="form-cont">
          <textarea class="tfarea" cols="30" rows="5" maxlength="300" v-model="tfareaWords" placeholder="최대 300자 이내" />
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit"
            >받으시는 분<span class="required"><span class="hidden">필수입력</span></span></strong
          >
          <span class="append"> <a href="#" class="btn-arrow">내 배송지</a> </span>
        </div>
        <div class="form-cont">내용내용</div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">추가 상품 옵션</strong>
        </div>
        <div class="form-cont">
          <div class="form-area">
            <div class="dropdown type-sel" :class="dropdown3 ? 'on' : ''">
              <button type="button" @click="dropdownToggle1" class="btn-drop">옵션을 선택해 주세요.</button>
              <ul class="option-drop add-prd-option">
                <li v-for="(item, index) in dropdownList1" :key="index">
                  <button type="button" @click="dropdownSelect1(item.id, item.option, item.price, item.addPrdNum), selected1(index)" :class="{ selected: item.selected }">
                    <strong class="option">{{ item.option }}</strong>
                    <span class="price">{{ item.price }}<span class="unit">원</span></span>
                  </button>
                </li>
              </ul>
            </div>
          </div>
          <ul class="add-prd-selected" v-if="dropdownSelected1.length > 0">
            <li v-for="(item, index) in dropdownSelected1" :key="index">
              <strong class="option">{{ item.option }}</strong>
              <b-numberinput :editable="false" min="1" v-model="dropdownSelected1[index].addPrdNum" class="inp-num small"></b-numberinput>
              <button type="button" class="btn-del" @click="deleted(item.id, index)"><span class="hidden">삭제</span></button>
            </li>
          </ul>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">
          <strong class="tit">주문 수량/요일 선택</strong>
        </div>
        <div class="form-cont">
          <div class="form-area">
            <div class="sel-day">
              <template v-for="(item, index) in selDateList">
                <div class="sel-item" :class="{ disabled: !item.choiced }" :key="index">
                  <span class="day">{{ item.day }}</span>
                  <input type="text" value="0" v-if="selDateList[index].oderNum == '+10'" />
                  <select v-model="selDateList[index].oderNum" v-else :disabled="!item.choiced">
                    <option v-for="(num, j) in item.numList" :key="j" :value="num">{{ num }}</option>
                  </select>
                </div>
              </template>
            </div>
            <div class="txt-assist type-reference">배송지마다 배송 가능 요일은 다를 수 있음</div>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">요일 선택 <span class="assist">(3일 선택)</span></div>
        <div class="form-cont">
          <div class="sq-area day">
            <span class="inp-sq" v-for="(item, index) in selDaliyList" :key="'selDaliyList-' + index">
              <input type="checkbox" :id="'selDaliyList-' + index" v-model="selDaliySelected" :value="item.day" @change="selDailyCheck(index)" /><label :for="'selDaliyList-' + index"
                ><span class="ftext">{{ item.day }}</span></label
              >
            </span>
          </div>
        </div>
      </div>
      <div class="form-item">
        <div class="form-tit">그린키트</div>
        <div class="form-cont">
          <div class="txt-assist small" v-if="selDaliySelected.length == 0">배송 요일을 선택해주세요.</div>
          <div class="sel-daliy" v-else>
            <template v-for="(item, index) in selDaliyList">
              <div class="sel-item" :key="index" v-if="item.selected">
                <span class="day">{{ item.day }}</span>
                <span class="sel">
                  <select v-model="item.selectOption">
                    <option v-for="(selOption, j) in item.selectOptionList" :key="j" :value="selOption">{{ selOption }}</option>
                  </select>
                </span>
                <b-numberinput v-model="item.numberinput" :editable="false" min="1" class="inp-num"></b-numberinput>
              </div>
            </template>
          </div>
        </div>
      </div>
    </div>
    <br /><br />
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
  radio1: any = ''
  radioList1: any = [{ value: '1회구매' }, { value: '정기배송' }]

  radio2: any = ''
  radioList2: any = [{ value: '1회구매' }, { value: '정기배송' }]

  radio3: any = ''
  radioList3: any = [{ value: '1회구매' }, { value: '정기배송' }, { value: '3333' }]

  radio4: any = '동의하지 않음'
  radioList4: any = [{ value: '동의함' }, { value: '동의하지 않음' }]

  radio5: any = ''
  radioList5: any = [{ value: '1회구매' }, { value: '정기배송' }, { value: '3333' }]

  radio6: any = ''
  radioList6: any = [
    { value: '1회구매' },
    { value: '정기배송' },
    { value: '동해물과 백두산이 동해물과 백두산이동해물과 백두산이동해물과 백두산이동해물과 백두산이동해물과 백두산이동해물과 백두산이동해물과 백두산이동해물과 백두산이' },
  ]

  checkbox1: any = []
  checkboxList1: any = [{ value: '1회구매' }, { value: '정기배송' }]

  checkbox2: any = []
  checkboxList2: any = [{ value: '1회구매' }, { value: '정기배송' }]

  checkbox3: any = ['1회구매']
  checkboxList3: any = [{ value: '1회구매' }, { value: '정기배송' }, { value: '3333' }]

  checkbox4: any = ['1회구매']
  checkboxList4: any = [{ value: '1회구매' }, { value: '정기배송' }, { value: '동해물과백두산이 마르고 닳도록<br>vc class예시입니다.v-html은 쓰지마세요<br>동해물과백두산이 마르고 닳도록' }]

  checkboxDay: any = []
  checkboxDayList: any = [{ value: '월' }, { value: '화' }, { value: '수', disabled: true }, { value: '목' }, { value: '금' }, { value: '토' }]

  select1: any = 'none'
  select2: any = 'none'
  select3: any = 'none'
  select4: any = 'none'
  select5: any = 'none'
  select6: any = 'none'
  selectList1: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]
  selectList2: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]
  selectList3: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]
  selectList4: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]
  selectList5: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]
  selectList6: any = [{ value: '1회구매' }, { value: '정기배송정기배송정기배송정기배송' }]

  selCall: any = 'none'
  selectCallList: any = [{ value: '055' }, { value: '02' }]

  selPhone: any = 'none'
  selectPhoneList: any = [{ value: '010' }, { value: '016' }]

  selDeliveryTime: any = 'none'
  selDeliveryTimeList: any = [{ value: '항상수고하십니다' }, { value: '문앞에 놔두세용' }]

  selDeliveryAsk: any = 'none'
  selDeliveryAskList: any = [{ value: '항상수고하십니다' }, { value: '문앞에 놔두세용' }]

  selEmail: any = 'none'
  selEmailList: any = [{ value: 'naver.com' }, { value: 'gmail.com' }]

  basicAddress: boolean = true

  numberinput: any = 1

  toggleMask: boolean = true

  checkboxCardNum: boolean = false

  tfareaWords: string = ''

  dropdown: any = false
  dropdownSelected: any = ''
  dropdownList: any = [
    { option: '옵션1', selected: false },
    { option: '옵션2', selected: false },
  ]

  dropdownToggle(): any {
    return (this.dropdown = !this.dropdown)
  }

  selected(index: any): any {
    return (
      this.dropdownList.map((obj: { selected: boolean }) => {
        obj.selected = false
      }),
      (this.dropdownSelected = this.dropdownList[index].option),
      (this.dropdown = !this.dropdown),
      (this.dropdownList[index].selected = true)
    )
  }

  dropdown3: boolean = false

  dropdownList1: any = [
    { id: 1, option: '내추럴플랜 클래식(450ml)', price: '1,700', selected: false, addPrdNum: 1 },
    { id: 2, option: '내추럴플랜 클래식(930ml)', price: '3,100', selected: false, addPrdNum: 1 },
  ]

  dropdownToggle1(): any {
    return (this.dropdown3 = !this.dropdown3)
  }

  selected1(index: string|number): any {
    return (this.dropdownList1[index].selected = true)
  }

  dropdownSelected1: any = []

  dropdownSelect1(id: any, option: any, price: any, addPrdNum: any): any {
    this.dropdown3 = !this.dropdown3
    const data: any = { id: id, option: option, price: price, addPrdNum: addPrdNum }
    if (
      this.dropdownSelected1.filter((e: { id: any }) => {
        return e.id == id
      }).length < 1
    ) {
      return this.dropdownSelected1.push(data)
    }
  }

  deleted(id: any, index: string|number): any {
    const num: any = this.dropdownList1.findIndex((x: { id: any }) => x.id == id)
    return (this.dropdownList1[num].selected = false), this.$delete(this.dropdownSelected1, index)
  }

  selDateList: any = [
    //선택가능 여부 choiced true: 선택가능, false : 선택불가능
    { day: '월', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: false },
    { day: '화', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: true },
    { day: '수', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: true },
    { day: '목', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: true },
    { day: '금', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: true },
    { day: '토', oderNum: 0, numList: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+10'], choiced: true },
  ]

  selDaliySelected: any = []
  selectOptionList: any = [
    '로스트비프 오리엔탈 샐러드 6,600원',
    '쉬림프 레몬파인 샐러드 6,600원',
    '블랙페퍼치킨 흑임자어니언 샐러드 6,600원',
    '닭가슴살햄 랜치시저 샐러드 6,600원',
    '콜라겐 with 샐러드 6,200원',
    '프로바이오틱스 with 샐러드 6,200원',
    '로스트비프 오리엔탈 샐러드+하루과일 9,200원',
    '쉬림프 레몬파인 샐러드+하루과일 9,200원',
    '블랙페퍼 흑임자어니언 샐러드+하루과일 9,200원',
  ]

  selDaliyList: any = [
    { day: '월', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
    { day: '화', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
    { day: '수', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
    { day: '목', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
    { day: '금', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
    { day: '토', selected: false, selectOption: this.selectOptionList[0], selectOptionList: this.selectOptionList, numberinput: 1 },
  ]

  selDailyCheck(index: string|number): any {
    return (this.selDaliyList[index].selected = true)
  }
}
</script>
<style lang="scss">
</style>
