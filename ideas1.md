## Introduction

인체와 동물, 공룡에 대하여 공부하고자 할 때, 책에 나와있는 글과 사진 만을 보고 그 모양을 이해하기 어려운 경우가 많다. 이를 해결하기 위해서 3D기기들을 이용하여 실제모양과 유사한 다양한 소재를 관찰과 조립을 통해 재미있는 학습을 가능하게 하는 3D 백과사전인 Real dict를 개발하고자 한다.

## Member

심재혁, 김성은, 정윤상, 최은정

## Research

- 목표
1) Leap motion과 looking glass를 이용한 실제감 있는 백과사전 어플리케이션을 통해 초등학생들의 학습을 도와주는 컨셉을 설정했다. 
2) looking glass로 물체를 입체적으로 보면서 leap motion을 통해 물체를 만지고 조립하는 등의 조작을 하여 물체의 구조를 학습하고 학습에 대한 흥미도를 높인다. 
3) 입체적인 모형을 조립함으로써 공간적인 지각을 높일 수 있다.

- 대상
학습에 흥미를 느끼지 못하는 초등학생, 중학생

##  Method

기기 > looking glass: A Holographics Display for 3D Creators, 
       Leap motion: 손을 인식하여 가상의 환경을 조종하는 기계 
       
프로그램 > unity: 3D 및 2D 환경을 개발하는 게임 엔진

## Development

- leapmotion 설치하는법
  : https://developer.leapmotion.com/get-started
    해당파일에있는 파일을 다운받은 후, 립모션 기기와 연결시켜 프로그램을 만들거나 작동시킬수 있다.
    
- looking glass의 구현원리
  : Looking glass회사에서 제공해주는 unity용 module을 import하여 화면을 looking glass에 나오게 했다. 바로 위의 사진을 보면 초록색 네모박스를 기준으로       looking glass화면이 나온다.
  
  
