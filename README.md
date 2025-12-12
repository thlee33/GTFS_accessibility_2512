# GTFS_accessibility_2512
GTFS의 역/정류소와 건물간 접근성 분석

## 대중교통 접근성 분석 및 시각화  
이 프로젝트는 GTFS(General Transit Feed Specification) 데이터와 건물 데이터를 활용하여 대중교통 접근성을 분석합니다.   
  
1. 주요 기능 및 특징  
  건물 단위 정밀 분석: OSM 건물 또는 건물통합정보를 사용하여 개별 건물 단위별 대중교통 접근성을 분석할 수 있습니다.   
    
  정류장 ID 패턴(BS: 버스, RS: 지하철)을 이용해 교통수단을 분류합니다.   
    
  분석 단계에서는 한국 표준 좌표계(EPSG:5179)를 사용하여 미터(m) 단위의 정확한 유클리드 거리를 산출합니다.  
    
  지도 시각화: V-World Midnight 타일을 배경으로 사용하여, 접근성 취약 지역(Magenta)과 양호 지역(Cyan)을 대비감 있게 표현합니다.    
  
2. 사전 준비 사항  
  이 코드를 실행하기 위해서는 다음의 파이썬 라이브러리가 필요합니다.  
  pip install pandas geopandas osmnx matplotlib contextily xyzservices   

  또한, 작업 디렉토리에 GTFS 파일인 stops.txt와 routes.txt가 위치해야 합니다.    
