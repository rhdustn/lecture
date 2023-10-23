# 지갑 구성 및 지갑의 역할

- 기본적인 역할로 암호화폐를 안전하게 보관할 수 있고 암호화폐를 전달하거나 받을 수 있다
- 자산의 소유권을 암호화 방식으로 증명 지갑의 개인키를 이용해서 거해릐 성명을 점증하고 본인의 자산을 관리
- 본인의 암호화폐의 보유량 확인
- 지갑의 거래내역 확인
- 복구 문구를 사용해서 지갑 복원(복구문구를 가지고 특정 알고리즘을 거쳐서 개인키를 추출한다)

## 금융

- 금융 쪽에는 장부를 가지고 모든 거래내역을 기록하는 방식
- 은행이라는 금융 기관은 장부에 거래내역을 의존할 수 밖에 없는 중앙 집관 방식

# 분산 원장
- 분산원장은 금융과 반대로 거래에 참여하는 모즌 참여자가 장부를 가지고 있고
- 거래가 발생했을대 해당 거래내역을 각자의 장부에 기록하는 방식
- 중앙에서 가지고 있는게 아니라 모두 장부를 가지고 관리한다

# 신원 인증 방식 분산 원장 기술로 개인키, 공개키, 서명(영수증)

## 암호화 방식

- 대칭형 : 암호화 복호화 할 때 사용하는 키가 동일한 키 1개를 사용한다<br>
암호화 한 사람과 수신하는 사람이 같은 키를 사용한다
- 비대칭형 : 사용하는 키와 복호화 할때 사용하는 키가 다른것 키 2개<br>
다른 사람에게 공개되어서는 정떄 안되는 키 (비밀키) 비밀키를 토대로 마든 공개키 한쌍

## 대칭형
- 나 -> 원본 -> 대칭키로 원본 암호화 -> 암호문
- 너 -> 암호문 -> 대칭키로 복호화 -> 원본
- 대칭형의 형태는 암호문을 대팅키를 가지고있는 사람은 누구나 전달이 가능하다.

## 비대칭형
- 비대칭형의 경우는 암호화 할때 공개키로 암호화
- 나 -> 원본 -> 너의 공개키로 암호화 -> 암호문
- 너 -> 암호문 -> 너의 개인 비밀키로 복호화 -> 원본

## 지갑의 공개키, 비밀키
- 공개키 : 사람들에게 공개할 키 정보를 암호화 할 때 사용
- 비밀키 : 본인만 알고 있어야 하는 키 암호문을 복호화할때 사용

# 비밀키와 공개키의 역할

비밀키 소유자가 비밀키로 데이터를 암호화 하고 공개키를 같이 전달한다
<br> 공개키와 암호문을 받은 사람은 공개키를 가지고 이용해서 검증이 가능하고
<br>이렇게 위험성이 있어 보이는 방법을 사용하는 이유가 데이터의 보호 목적보다는
<br>공개키 데이터를 제공한 사람의 신원을 보장해주기 위해서
<br>암호화된 데이커다 공개키로 복호화 된다는 것이 공개키와 쌍으로 이루는 비밀키에 의해서
<br>암호화가 되었다는 뜻 데이터의 제공자가 맞는지 이사람이 이 서명을 한 사람인지 검증
<br>이 방법이 공인 인증 체계의 기본 바탕의 전자 서명

# 개인키 
- 실제 블록체인 네트워크에 개인키를 생성하는 방식은 <br>
2진수로 랜덤값을 64자리의 16진수 값으로 만든 것이 개인키
- 개인키가 겹칠수는 있는데 확룰이 턴문학적으로 낮아서 무시를 하고있다
- 나올 수 있는 확율이 개인키의 경우의 수는 2^256개의 개인키(지구상 전체 원자수 보다 많다)

# 순서
- 1. 암호화 하고 싶은 데이터를  SHA256 방식으로 해싱하고
- 2. 개인키를 사용해서 해시값으로 서명을 생성
- 3. 서명이랑 공개키는 제 3자에게 전달이 되고
- 4. 받은 제3자는 공개키를 이용해서 서명을 검증

# 개인키 공개키 한쌍 키 생성할 떄 ECC타원 곡선을 사용

- 타원 곡선 수학을 기반으로 디지털 서명을 보호하기 이해 사용하는 암호화 기숳
- 공개키와 개인키의 개념이 있고 공개키는 암호화와 검증에 사용, 개인키는 복호화 서명을 만들때 사용
- 디지털 서명을 본인이 개인키로 메시지로 서명을 할 수 있고 공개키는 받은 사람이 누구나 서명을 확인해 볼 수 있다
- 쉽게 말해서 암호화 및 해독에 사용<br>
- 다은사람의 공개키로 암호화해서 전달을 하면 그 사람의 개인키로만 복호화가 가능하고<br>
당사자씨리의 데이터 기밀성 보장
- 디지털 서명을 본인의 개인키로 생성 하고 다른사람한테 전달해서 공개키와 함께 서명을 검증할 수 있는 무결성 보장
- 어려운 수학문제...

-  y^2 = x^3 + ax +b
- 기준점이 있고 기준점에서 개인키를 가지고 공개키를 구하는데 기준점과 공개키로 개인키를 역산하기 힘들다.