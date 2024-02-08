# 프로젝트 목적

이 프로젝트는 서울 부동산 시장에 대한 심층적인 분석과 인사이트를 제공하는 인터랙티브 대시보드를 개발하는 것을 목표로 합니다. 이 대시보드는 부동산 투자자, 중개인, 에이전시 및 일반 구매자와 판매자를 포함한 다양한 사용자 그룹을 대상으로 합니다. 대시보드를 통해 사용자는 서울 아파트 매매 데이터를 다양한 각도에서 분석하고, 시장 트렌드와 패턴을 파악할 수 있습니다. 이를 통해 지역별 매매 데이터를 시각적으로 탐색하고, 데이터 기반의 의사결정을 지원받을 수 있습니다.

---

## 팀원 소개
- **송 민**: [GitHub](https://github.com/ms2063)
- **송준호**: [GitHub](https://github.com/Kongalmengi)
- **임예원**: [GitHub](https://github.com/dsmondo)
- **한대희**:  [GitHub](https://github.com/roklp)

---


## 개발 환경
본 프로젝트는 다음 환경에서 구현되었습니다:
- **Programming Languages**: Python (ver. 3.12.1)
- **Web Framework**: Streamlit (ver. 1.31.0)

프로젝트는 Python이나 Streamlit의 다른 버전을 사용하여도 작동할 수 있습니다. 그러나 최적 호환성을 위해 제공된 `requirements.txt`에 명시된 버전 사용을 권장합니다.

---


## 주요 라이브러리
라이브러리 목록은 [requirements.txt](https://github.com/suhyeon0325/SeoulREDash/blob/main/requirements.txt)에서 확인 가능합니다.

---


## 데모 페이지
대시보드 데모: [서울 부동산 인사이트 대시보드](https://miniproject-6qhdygprketeard33iurkp.streamlit.app/)

---


## 주요 기능
데이터 처리 및 시각화를 위해 개발한 주요 메서드:
- `MAP_TOKEN`: 환경 변수에서 불러온 맵 토큰입니다.
- `load_geo_data()`: GeoJSON 파일에서 지리 데이터를 로드하는 함수입니다.
- `load_data()`: CSV 파일에서 데이터를 로드하는 함수입니다.
- `plot_mapbox()`: 서울특별시 시군구별 아파트 매매 지도를 시각화하는 함수입니다. 사용자에게 평균 물건 금액, 평균 건물 면적, 평균 건축년도 등의 정보를 포함한 지도를 제공합니다.
- `select_area()`: 사용자로부터 구와 동을 선택받는 함수입니다. 이를 통해 사용자가 관심 있는 지역의 데이터를 세밀하게 조회할 수 있습니다.
- `main()`: 대시보드에 서울특별시 아파트 매매 거래 지역별 정보를 시각화하는 주 함수입니다. 이 함수는 대시보드의 구조를 정의하고, 위에서 언급한 다른 함수들을 호출하여 사용자에게 데이터를 시각화하고 제공합니다.

---


### 상세 설명
- **`main()`**: 대시보드의 제목을 설정하고, GeoJSON 및 CSV 데이터를 로드하여 서울의 아파트 매매 데이터를 시각화합니다. 사용자는 지역별 매매 데이터를 볼 수 있으며, 다양한 필터 옵션을 통해 데이터를 세밀하게 조사할 수 있습니다.
- **`load_geo_data()`**: GeoPandas를 사용하여 GeoJSON 파일을 읽고, GeoDataFrame으로 반환합니다. 반환된 GeoDataFrame은 서울특별시의 지역별 경계 및 기타 지리적 정보를 포함하고 있으며, 대시보드에서 지도 시각화에 사용됩니다.
- **`load_data()`**: Pandas 라이브러리를 사용하여 CSV 파일을 읽고, DataFrame으로 반환합니다. 이 DataFrame은 서울특별시 아파트 매매 거래에 관한 데이터를 포함하고 있으며, 대시보드에서 다양한 분석 및 시각화에 활용됩니다.
- **`plot_mapbox()`**: 이 함수는 Mapbox를 활용하여 서울특별시 내 시군구별 아파트 매매 정보를 지도 위에 시각화합니다. 사용자는 지도 상의 점들을 통해 각 지역의 평균 물건 금액, 평균 건물 면적, 평균 건축년도를 확인할 수 있습니다. 점의 크기와 색상은 해당 지역의 아파트 매매 가격 및 건물 면적을 나타냅니다.
- **`select_area()`**: 이 함수는 사용자에게 구와 동을 선택할 수 있는 옵션을 제공합니다. 사용자는 드롭다운 메뉴를 통해 관심 있는 지역을 선택할 수 있으며, 이 선택은 나머지 대시보드의 데이터 필터링에 사용됩니다.


---


## 발표자료 PDF
팀 프로젝트의 발표자료는 여기에서 확인할 수 있습니다: [서울 부동산 시장 인사이트 대시보드.pdf](https://github.com/suhyeon0325/SeoulREDash/blob/main/%EC%84%9C%EC%9A%B8%20%EB%B6%80%EB%8F%99%EC%82%B0%20%EC%8B%9C%EC%9E%A5%20%EC%9D%B8%EC%82%AC%EC%9D%B4%ED%8A%B8%20%EB%8C%80%EC%8B%9C%EB%B3%B4%EB%93%9C_2%EC%A1%B0.pdf)

---


## Release Notes
개발 릴리즈 노트는 [Releases](https://github.com/suhyeon0325/SeoulREDash/releases) 섹션에서 확인하세요.

---


## License
이 프로젝트는 [MIT License](https://github.com/suhyeon0325/SeoulREDash/blob/main/LICENSE)에 따라 라이센스가 부여됩니다.
