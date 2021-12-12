# PROJECT1> DATA ANALYSIS _ 게임 데이터 분석
  - 주제: 다음 분기에 어떤 게임을 설계해야 할까?
  - 주어진 데이터:게임 이름/플랫폼/출시 연도/장르/제작 회사/지역 별(북미, 유럽, 일본, 기타) 출고량
  
  - 목차
  1. 데이터 전처리
  2. 데이터 분석
     1. 지역에 따라서 선호하는 게임의 장르가 다를까?
        - 북미지역은 Platform, 유럽지역은 Shooter, 일본지역은 Role-Playing, 기타지역은 Shooter이 평균적으로 큰 출고량을 차지함
        - 일본지역을 제외한 나머지 세 지역에서는 platform, shooter, sports, racing이 출고량이 높았고 이를 제외한 다른 장르도 거의 비슷한 형태를 보임 -> 선호하는 게임 장르가 유사함
        - 결론: 만약에 새로운 게임을 북미지역, 유럽지역, 기타지역에서 출시한다면, Shooter장르, Platform장르가 좋을 것으로 판단되며, 일본에서는 shooter 장르를 출시하지 않는 것이 좋을 것으로 보임
     2. 연도별 게임의 트렌드가 있을까? 
        - 연도 별 게임 전체 트렌드: 연도별 총 출고량을 확인한 결과, 과거부터 출고량이 지속적으로 상승하다가 1995년부터 급격히 상승하여 2007-2009년 전 후로 정점을 찍고, 급격히 출고량이 감소하는 양상을 보임
        - 연도 별 게임 장르 트렌드
          - 어떤 장르가 크게 증가했을까?
            - 연도 별로 각 장르의 총 출고량을 그래프로 확인해본 결과, Action, Sports, Shooter, Misc은 2010년 전후로 크게 출고량이 증가
          - 연도 별로 어떤 장르가 가장 많이 출시되었을까?
            - 각 년도마다 최대 count인 장르를 추출해 분석한 결과, 1994년부터 2002년까지 Sports 장르가 가장 많이 출시되었고, 2003년부터 2016년도에 Action 장르가 가장 많이 출시됨
          - 연도 별로 어떤 장르의 출고량이 가장 많았을까?
            - 각 년도마다 최대 출고량인 장르를 추출해 분석한 결과, 2007년부터 2012년에는 Platfrom 장르의 출고량이 가장 많이 차지했고, 비교적 최근인 2013년부터 2016년도까지 Shooter 장르의 출고량이 가장 많았음
        - 결론
          - 전체 트렌드 분석 결과, 전반적인 트렌드는 감소하는 형태
          - 연도 별 게임 장르 트렌드 분석결과, 2003년 ~ 2016년에 Action 장르가 가장 많이 출시되었으나, 출고량을 확인해본 결과, 2007 ~ 2012년에는 Platform 장르의 출고량이 가장 많았고, 2013~2016년에도 역시 Action 장르가 아닌 Shooter 장르의 출고량이 가장 많았음
     3. 출고량이 높은 게임에 대한 분석
        - (전 시기) 출고량 제일 많은 게임 5개: Wii Sports, Super Mario Bros., Mario Kart Wii, Wii Sports Resort, Pokemon Red/Pokemon Blue
          - 특이점: 이 중 세 게임의 플랫폼은 'Wii'이고, 제작 회사는 5 개 모두 'Nintendo'
        - 최근 10년 내에 출시된 게임 중 출고량 제일 많은 게임 5개: Kinect Adventures!, Grand Theft Auto V, Grand Theft Auto V, Call of Duty: Modern Warfare 3, Call of Duty: Black Ops
          - 특이점: 이 중 네 게임의 플랫폼이 'X360'이고, 장르는 'Shooter', 'Action'이 각각 2개씩 차지
        - 최근 10년 내 출시된 게임 중 평균 출고량이 높은 장르 순위: Shooter, Platform, Sports
          - 과연 출고량에서 유의미한 차이가 있을까? (Anova Test/T-test)
            - 출고량 상위 3개의 장르 평균을 비교하기 위해 ANOVA 검정 및 T-test 시행 결과, Shooter, Platform의 출고량 평균의 차이는 유의미하지 않고, Platform은 Sports에 비해서 높다는 것을 알 수 있음
        - 최근 10년 내 출시된 게임 중 평균 출고량이 높은 플랫폼 순위: PS4, X360, PS3
          - 최근 10년 내 출시된 게임 중 Shooter 장르의 출고량이 가장 많은 플랫폼: X360
          - 최근 10년 내 출시된 게임 중 Platform 장르의 출고량이 가장 많은 플랫폼: NES
          - 장르와 플랫폼 사이에는 연관이 있을까?
            - 카이스퀘어 검정 결과, 플랫폼과 장르 사이에 연관성은 없다.
      - 결론
        - 최근 10년 내 출시된 게임 중 출고량이 많았던 5개의 게임 중 4 개의 플랫폼은 'X360'임. 
        - 최근 평균 출고량이 높은 장르 순위는 Shooter, Platform, Sports이었고, 이들 중 Shooter, Platform이 평균적으로 높았다. 
        - 마지막으로, 물론 장르와 플랫폼 사이에 연관성은 없어 특정 플랫폼이 특정 장르를 독점하고 있지는 않지만, 최근 Shooter 장르의 출고량이 가장 많았던 플랫폼은 'X360', 최근 Platform 장르의 출고량이 가장 많은 플랫폼은 'NES'로, 만약 Shooter 장르의 게임을 출시한다면 'X360'플랫폼을, 만약 Platform 장르의 게임을 출시한다면 'NES' 플랫폼을 선정하는 것이 좋다고 판단
      
  3. 데이터 분석 결과
      - 게임 장르: Shooter 혹은 Platform 장르 선정
      - 게임 지역: Shooter의 경우, 일본 지역을 제외한 전 지역에서 출시하고, Platform의 경우, 일본 지역을 포함한 전 지역에서 출시
      - 게임 플랫폼: Shooter 장르 출시할 경우 'X360' 플랫폼과 협력, Platform 장르 출시할 경우 'NES' 플랫폼과 협력



PROJECT2> MACHINE LEARNING - 미세먼지 수치 예측 모델

PROJECT4> DEEP LEARNING - 네이버 쇼핑 리뷰 데이터 감성 분석 
