# 주제 선정

### 데이터 분석가 채용 공고를 보면 경력직을 정말 선호하는 것 같다.

- 데이터 분석가 경력이 오를수록 지원할 수 있는 기업 형태 수 차이는 어떻게 될까?
- 데이터 분석가 경력이 오를수록 지원할 수 있는 기업의 연봉 차이는 어떨까?



### 데이터 수집

취업포털 사이트 사람인 - '데이터 분석' 검색 결과 크롤링

https://user-images.githubusercontent.com/69154643/106712482-5bd9bf80-663c-11eb-8624-40c1b869f566.mp4
-> 작동 화면

한 번의 크롤링으로 모든 변수를 포함한 대용량 데이터를 수집하고 싶었으나

경력(15)*지역(180)*기업형태(18)*연봉(15)*복리후생(100) * html 업데이트 2초

약 **4만 시간**이 필요하게 되어

다음과 같이 변수별로 나눠 크롤링을 진행, csv 파일을 확보하였다.

1. 경력 - 기업 형태 - 복리후생 - 검색결과
2. 경력 - 연봉 - 검색결과
3. 지역 - 연봉 - 검색결과
4. 지역 - 복리후생 - 검색결과
5. 지역별 기업수

실습을 위해 대용량 데이터라 가정하고,
Centos7을 통해 MariaDB와 연동해보았다.

![koo](https://user-images.githubusercontent.com/69154643/106714481-4023e880-663f-11eb-8ed9-a22cc0e591dd.JPG)

### 데이터 분석 & 시각화

![bwtt-tile](https://user-images.githubusercontent.com/69154643/106743554-e680e580-6661-11eb-8d4f-5218f35659cc.JPG)


- 중소 기업의 수가 압도적으로 높게 나타났다.

- 또한 우수 기업, 수출입 기업이 높게 나타났다.

- 신입으로 대기업, 매출1000대 기업, 금융기관, 공기업, 교육기관, 코스피, 코넥스에 입사하는 경우는 극히 드물 것으로 보인다.

- 신입에는 약 1200개의 중소 기업을 지원할 수 있었는데, 2년차가 되면 지원할 수 있는 중소 기업이 2500을 넘어 2배 이상의 차이를 보이고 있다.

- 5년차부터는 3000개 이상으로 넘어가며 의외로 5년차와 10년차 사이의 큰 차이는 보이지 않는다.

- 또한 경력이 아무리 쌓여도 금융 기관, 공기업, 교육기관, 코스피, 코넥스에서는 선호하지 않는 듯 하다.

![해1-tile](https://user-images.githubusercontent.com/69154643/106747093-c869b400-6666-11eb-839d-544cf13a23f8.JPG)

- 중소 기업의 수가 너무 많았기 때문에 다른 기업 형태 수 변화가 잘 눈에 띄지 않아 기업 형태별로 따로 시각화해봤을 때

- 모든 기업들이 신입 ~ 2년차까지 경력에 따른 선호도가 가파르게 올랐으며, 신입과 2년차의 차이는 적게는 약 1.5배, 크게는 2.5배 정도로 나타났다.

- 2년/4년차 역시 선호도가 차이가 심하지만 공통적으로 2년차-3년차 간의 차이는 작은 것으로 나타났다.

- 즉, 첫 이직을 할 경우에 2년의 경력을 쌓고 하는 것이 가장 이상적이라는 것을 알 수 있다.

- 1년차-2년차의 선호도의 차이가 크기 때문에 1년 더 기다리면 이직 기회가 훨씬 많으며, 2년차-3년차의 선호도는 거의 차이가 없기 때문에 비효율적이기 때문이다.

- 만약 3년차일 경우라면, 1년을 더 기다려서 4년차가 된 후 이직을 하는 것이 이상적이다.

- 4년차~10년차는 경력에 따른 선호도 차이가 크게 없기 때문에 4년차 이후 더 이상 경력으로 인한 추가적인 메리트는 줄어들었다는 점을 인식해두면 좋다.
