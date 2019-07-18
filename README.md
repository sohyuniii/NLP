## NLP (Natural Language Processing, 자연어처리)

### [3. Feature representation](https://github.com/sohyuniii/NLP/blob/master/3.%20Feature%20representation.ipynb)
- 피처 엔지니어링 : 원시 텍스트 데이터, 코퍼스로부터 텍스트 분석을 위해 도움이 되는 특성을 생성하는 과정
- 문서의 내용을 대표할 수 있는 단어만 선택에 입력변수로 사용 -> feature selection
- 텍스트를 컴퓨터로 처리하기에 적합한 형태로 변환 -> **feature representation**
    - 단어를 숫자로 -> **word embedding*** : 빈도기반(*TF,TF-IDF*) / 확률기반(*Word2vec, Glove*) 
 ##### BoW (Bag-of-Words) = TF
   - 자연어 처리에서 널리 쓰이는 가장 기본적인 방법
   - 전체 단어 개수만큼 차원을 갖는 벡터 생성
 ##### TF-IDF (Term Frequency-Inverse Document Frequency)
   - 흔히 나오는 단어는 데이터에 잡음만 더해질 수 있기 때문에 이를 해결
   - 문서별로 자주 등장하는 단어는 낮은 가중치, 드물게 나오는 단어는 높은 가중치를
   - 단어 빈도와 문서 빈도 역수를 사용해 가중치를 생성
   - 문서 길이의 영향력을 감소시키기 위해 TF에 대한 표준화 또는 정규화수행 -> IDF 계산과 무관
 ##### N-gram
   - 전체 문자열을 N값 만큼 sub string으로 나누어 사용하는 방법
   - 여러 단어로 이뤄진 구와 절의 의미를 포함할 수 있다.
   - N이 늘어날수록 학습에 필요한 데이터가 기하급수적으로 늘어남
