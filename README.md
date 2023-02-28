# '슬램덩크' 키워드 네이버 블로그 - 워드 클라우드 제작
- 네이버 블로그 글에 있는 텍스트로 워드 클라우드 시각화를 하였음

1. 프로젝트 소개
- 기술 스택 : 파이썬 (라이브러리 : 셀레니움, 워드 클라우드)
- 목적 : 마케팅 기획을 위한 자료로 쓰일 수 있는 데이터 분석, 시각화
- 내용 : 네이버 블로그에서 '슬램덩크'로 검색을 한다. 나온 글들을 차례로 크롤링 한 다음에 그 단어들로 워드 클라우드 시각화를 한다.

2. 분석 결과
- 농구, 만화, 구매, 일본, 밥, 정대만, 강백호 등의 단어가 눈에 띈다. 
- 마케팅에 활용할 만한 단어가 나오지는 않았다.
- 네이버 블로그 특성 상 일상 단어가 대부분임. (ex. '엄마', '밥' 등)
- 기대했던 것은 "'최고심', '뉴진스' 이런 단어가 함께 언급된 것으로 수량적으로 확인이 가능하다. 이를 콜라보 마케팅 근거 자료로 쓸 수 있겠다." 이런 것이었음.

3. 분석 프로세스
- 크롤링 : 네이버 블로그 글을 크롤링 대상으로 하였다. 범위는 글 140개였음. (페이지당 글이 7개이고 총 20페이지를 했다.) 처음에 블로그 글을 보았을 때 슬램덩크를 보러 갔다 온 사람들이 자신의 일상을 적으면서 소비한 품목이나 선호하는 취향, 아이템을 함께 적은 사람들이 많았다. 그래서 100개 이상의 글을 합쳐서 데이터 분석을 하게 된다면 여러 사람이 공통적으로 소비하는 아이템을 파악할 수 있을 것이라고 생각했다.
- 전처리 : ('것', 407), ('나', 390), ('내', 293), ('때', 267), ('이', 261), ('거', 260),  ('안', 229), ('더', 221), ('수', 218) 등 데이터 분석 목적에 맞지 않는 의미 없는 단어들을 삭제함. 한글자 단어 중에 의미 있는 단어도 있다고 생각해서 한글자 단어를 모두 없애지는 않았다. '아이유', '아키타' 이런 단어가 있었는데 확인해보니 하나의 글에서만 20번씩 언급되어서 워드 클라우드에 나온 것이었기에 삭제함.
- 시각화 : wordcloud 라이브러리를 사용했다.

4. 한계 및 해결 과제
- 마케팅에 도움이 될 만한 데이터 분석은 무엇일지 더 탐구해봐야할 것이다. '나는 최고심이랑 슬램덩크를 콜라보 할 거야!' 라는 명확한 주장을 먼저 정하고 그를 뒷받침하는 근거를 도출하는 데이터 분석을 해도 좋을 것 같다. 이를 수행하려면 내가 한 작업량의 50배는 더 해야할 것 같다.
- 문제점을 발견했는데, 여러 글이 아니라 하나의 글에서만 언급한 단어가 언급량 상위권 단어로 나오니까 정확한 분석을 방해하였다. '아이유', '아키타' 같은 이슈를 방지하기 위해 적어도 5개 이상의 글에서 언급되는 것으로 필터링 할 필요가 있었음.

5. 레퍼런스
- https://soso-bigdatamarketing.tistory.com/42
