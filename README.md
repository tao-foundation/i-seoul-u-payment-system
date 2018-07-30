# I-Seoul-U Payment System

본 제안서는 대한민국의 소.상공인에게 수수료 0% 의 결제 시스템을 도입하고자 하는 서울시에 제안하는 시스템입니다.

아울러, 본 제안서는 그 어떤 카피라이트 , 특허 License 가 없습니다.

MIT 및 GNU GPL V3 의 Lesser 를 적용합니다.

누구나, 관심있는분은 포크 하셔서 사용하셔도 되고, 좋은 방안이 있으면 issue 로 토론에 참여해 주시면 감사합니다.

## 1. Executive Summary

 - 제안 목적 : 현행 중앙화된 카드/VAN 업체의 과도한 수수료를 줄이는 기술방안을 제시함. 서울시의 카드수수료 0%, 정부의 중소상공인 카드 수수료 1%이하대로 인하를 만들기 위한 기술적방안제시.

 - 제안 기술 : TPS 와 트랜잭션 수수료가 낮고, 보안 유지 비용을 극소화 하는 POA / DPOS 블록체인을 기반으로 , 퍼블릭이 아닌 Private 노드로서 제한된 Community [서울시,금융권,IT업체,상공인연합회, ..] 이 각각의 노드를 유지 관리한다.

 - 전체 노드는 16개 이하로 유지하여 TPS 및 컨펌 속도를 유지하고, 이는 제한적 Access를 유지하는 준 Private Blockchain 으로서, 기존의 VAN/POS 사의 독점적인 망 수수료 에 대응되는 커뮤니티 기반의 공유형 블록체인을 이용한다.

 - KRWT (KRW Tether) 형태의 블록체인 기반 토큰을 생성하여, 이를 실제 금융화폐 (KRW) 의 지급을 기록하는 용도로 사용한다.

 - 기존, DPOS / POA 퍼블릭 체인과의 차이점은 , Stake 에 의한, 블록생성자/노드 관리자에 대한 불필요한 보상을 무위화 하여, 노드의 관리비용은 별도의 KRW 로 비용으로 산정한다.

 - 결론적으로, 블록체인의 화폐를 담는 퍼블릭체인이 아닌, 트랜잭션의 보안 비용과 시스템 유지 비용을 최소화 하고, 분산,공유처리용도로 체인을 이용할 뿐, 이는 정상적인 의미의 블록체인기술이 아님을 주지하기 바랍니다.

## 2. 기존 VAN 과의 시스템 구조의 차이점.

 ### 기존 VAN 

 1) 중앙화
 2) 트래픽 집중화
 3) 보안 유지 비용 ↑
 4) 내부자 위조 가능성
 5) 전산시스템 구축비용 ↑
 6) 모빌리티 ↓

  #### BM관점 독점과 고비용초래

  1) 중앙집중화 통계정보 독점
  2) 3rd party 응용부족
  3) 개인정보 보호취약


 ### 제한된 Private 체인

 1) 분권화(분산화)
 2) 트래픽 분산 
 3) 보안 유지 비용 ↓
 4) 내부자 위조 불가
 5) 전산시스템 구축비용 ↓
 6) 유연성 ↑

  #### BM관점 다양한 ECO가능 -> 2차,3차 파생서비스 산업가능

  1) 통계정보의 공개화로
  2) 3rd party 응용및 통계서비스 활성화
  3) 개인정보보안성 극대화

## 3. 기존 금융시스템과의 연계방안.

  ### Fig. 노드 / Payment Gateway 연계 방안.
  ![](assets/payment-node-interface.PNG)

 ### 파생 연계 산업 리스트

  1) 노드 및 시스템 구축비용 수수료 부분은 0% 로 줄이고, 세원노출이 잡히므로, 국세청에서 서울페이먼트 이용시, 소액결제 부분에 대해서 1.5% 부가세 삭감해준다.
  2) 1%는 상공인 , 소비자에게 return.
  3) 0.5% 는 시스템 유지 보수 운영비용으로 이용.
  4) 고액 결제의 경우는 2~3% 수수료를 받는다. 이 부가수익으로 소액 , 소상공인 결제 부분에 Compensation
  5) 체인에 기록된 공개 블록데이터(장부데이터) 기반 통계 및 마케팅, 타켓 홍보를 전담하는 산업군이 발생함.
  6) 체인에 기록을 기반으로 제2, 제3의 통계 서비스가 가능하고, 이를 가공하여 필요한 판매자에게 부가산업을 생성함.
  7) 기존 VAN 사 단말기 대체할 게이트웨이 및 기존 단말 upgrade 및 교체 수요 발생. <br>
  소규모 장치 개발산업이 활성화된다.
  8) 모든 소프트웨어와 결제시스템, 규격을 OpenSource 화 하여, 누구나 좋은 개선방안, 새로운 Eco 를 창출하고자 하는 사업자, 독립개인 사업자, 개인 모두에게 새로운 산업가치 창출에 도움이 되도록 한다.
  9) 아울러, 블록체인의 기반 기술을 제한적으로 활용하여 그 효과를 확인하고, 유관 산업에 기반이 될수 있는 테스트베드와 기초 기술 테스트베드가 된다.
  10) 멀티플 체인을 활용하여, Load Balancing 을 활수 있도록 향후, 늘어나는 수요에 맞춰서 Scalable 하게 별도 독립 체인을 Fork 하여 state 를 공유하게 할수있다.


## Copyright
Copyright and related rights waived via CC0.




  


