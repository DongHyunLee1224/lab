#  **Naver 영화 리뷰 감정 분석**
### Naver의 영화 리뷰 데이타를 이용하여 리뷰에 긍정 / 부정을 예측

# **설명**
BERT(Bidirectional Encoder Representations from Transformers)는 구글이 개발한 사전훈련(pre-training) 모델입니다. 이 모델을 이용하여 한글로 된 Naver 영화 리뷰를 분석 하고 리뷰 내용에 대하여 긍정과 부정을 식별하는 모델을 구현 하였습니다.

이 모델은 bert-base-multilingual-cased 모델을 사용 하였습니다. bert-base-multilingual-cased 모델은 한국어 포함 104개의 언어처리가 가능한 모델로 단어 사전의 크기가 11만개가 넘습니다.

- 데이터 출처 : https://github.com/e9t/nsmc.git)
- 참고 코드 : https://github.com/deepseasw/bert-naver-movie-review

# **실행 방법**
1.   개인 구글 드라이브에 아래 파일을 업로드 합니다. 
     * Naver_emotion_analysis.ipynb 
     * ko_data.csv 

2.   Naver_emotion_analysis.ipynb 파일을 Colab을 통하여 편집 합니다. 
     * 아래 DATA_PATH 부분에 본인이 업로드 한 경로 지정 합니다. 
    ![DATA_PATH](https://user-images.githubusercontent.com/76559418/103089424-403ccb80-4631-11eb-8fb4-a97333a9c67f.JPG)
    
3. 상단 메뉴에서 런타임 -> 런타임 유형 -> 하드웨어 가속기 -> GPU로 변경 후 저장 합니다.

4. 런타임 -> 모두실행을 통하여 소스를 실행 합니다.

5. 드라이브 마운트를 위하여 결과 창에 링크가 보이면 해당 링크에 접속 하면 키를 복사 할 수 있습니다. 키를 복사 한 후 결과창에 붙여 넣으면 마운트가 됩니다.

