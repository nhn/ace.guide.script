# AceCounter+ Script
AceCounter+ 분석 서비스를 사용하기 위한 설치 스크립트 입니다.
* [Acecounter Plus 서비스 페이지 바로가기](https://new.acecounter.com)(회원가입 및 로그인 필요)
* [설치 가이드 바로가기](https://github.com/nhnent/ace.guide.script/wiki)

# 간편 시작하기
AceCounter+를 가장 쉽게 이용하는 방법입니다.  
  
`설치 스크립트` 다운로드 하기 :
1. https://new.acecounter.com 접속
2. 로그인
3. 서비스 관리 클릭
4. 분석스크립트 클릭
5. 서비스 목록 중 `Web Free`, `Web Trial`에서 다운로드 버튼 클릭
6. 압축 해제 후 `AceCounter Plus_Script_v9.txt` 파일 열기  
<p>
`공통.js`파일 생성하기 (선택사항) :
```javascript
var _AceTM = (function (_j, _s, _b, _o, _y) {
    var _uf='undefined',_pmt='',_lt=location;var _ap = String(typeof(_y.appid) != _uf ? _y.appid():(isNaN(window.name))?0:window.name);var _ai=(_ap.length!=6)?(_j!=0?_j:0):_ap;if(typeof(_y.em)==_uf&&_ai!=0){var _sc=document.createElement('script');var _sm=document.getElementsByTagName('script')[0];
    var _cn={tid:_ai+_s,hsn:_lt.hostname,hrf:(document.referrer.split('/')[2]),dvp:(typeof(window.orientation)!=_uf?(_ap!=0?2:1):0),tgp:'',tn1:_y.uWorth,tn2:0,tn3:0,tw1:'',tw2:'',tw3:'',tw4:'',tw5:'',tw6:'',tw7:_y.pSearch};_cn.hrf=(_cn.hsn!=_cn.hrf)?_cn.hrf:'in';for(var _aix in _y){var _ns=(_y[_aix])||{};if(typeof(_ns)!='function'){_cn.tgp=String(_aix).length>=3?_aix:'';_cn.tn2=_ns.pPrice;_cn.tn3=_ns.bTotalPrice;_cn.tw1=_ns.bOrderNo;_cn.tw2=_ns.pCode;_cn.tw3=_ns.pName;_cn.tw4=_ns.pImageURl;_cn.tw5=_ns.pCategory;_cn.tw6=_ns.pLink;break;};};_cn.rnd=(new Date().getTime());for(var _alx in _cn){
    var _ct=String(_cn[_alx]).substring(0,128);_pmt+=(_alx+"="+encodeURIComponent((_ct!=_uf)?_ct:'')+"&");};_y.acid=_ai;_y.atid=_cn.tid;_y.em=_cn.rnd;_sc.src=((_lt.protocol.indexOf('http')==0?_lt.protocol:'http:')+'//'+_b+'/'+_o)+'?'+_pmt+'py=0';_sm.parentNode.insertBefore(_sc,_sm);};return _y;
})(0,'0', 'atm.acecounter.com','ac.js',window._AceTM||{});
```
`AceCounter Plus_Script_v9.txt`의 내용을 별도의 공통 파일로 생성해주세요.  
<p>
AceCounter+ 설치 스크립트 노출하기 :  
**Test.html**
```html
<footer>
    <script type="text/javascript" src="공통.js"></script>
</footer>
```
설치 스크립트는 다른 영역도 상관 없으나 가급적 `footer`영역에 노출 시키기를 권장드립니다.
