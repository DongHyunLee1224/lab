# **Sentiment Analysis with BERT**
미드 Friends 대화 내 화자의 감정 분류 및 예측

# **설명**
bert-base 모델은 12개의 transformers 블록을 가진 인코더로 구성되어 있습니다.   
인코더의 각 블록에 대해 768차원의 hidden layer가 포함되어 있어 총 110M 의 매개 변수가 생성됩니다.    
기본 모델은 최대 512개의 토큰 입력을 허용하고, 벡터 표현을 출력합니다.    
또한 Bert는 masked LM 기술을 구현하는데, 각 입력 문장에 대해 처음에는 ‘[CSL]’ 입력을 허용하고,   
문장의 끝 부분에는 특수 분리 토큰 ‘[SEP]’를 삽입한 후 무작위로 masking 할 단어를 선택합니다.

BERT 모형을 활용해, 미드 Friends의 대화 내 화자의 감정을 분류 하고 예측해 보는 모델을 구현 하였습니다.  
이 모델은 bert-large-uncased 모델을 사용하였으며 large모델의 경우 1024개의 hidden layer를 가지고 있습니다.

  - 데이터 출처 : http://doraemon.iis.sinica.edu.tw/emotionlines/index.html
  - 참고코드 : https://colab.research.google.com/drive/1EMzEfTYjYLgEHjCCP1vEr9oOZLXMocGh?usp=sharing 
 
 
# **데이터**
  - 파일은 speaker , utterance , emotion , annotation 4개로 구성 되어 있으며 8개의 감정으로 분류 되어 있습니다.
  
    - speaker : 화자
    - utterance : 대화 내용
    - emotion : 대화내용으로 분류된 감정 label  
    
  - 전체 14,503개의 대화 내용이 있습니다.  
  
    - friends_train.json : 10,561
    - friends_dev.json : 1,178
    - friends_test.json : 2,764

# **실행 방법**
1.   개인 구글 드라이브에 아래 파일을 업로드 합니다.  

     * Friends_emotion_analysis.ipynb 
     * en_data.csv
     * friends_train.json
     * friends_dev.json
     * friends_test.json

2.   Friends_emotion_analysis.ipynb 파일을 Colab을 통하여 편집 합니다. 
     * 아래 DATA_PATH 부분에 본인이 업로드 한 경로 지정 합니다.  
    ![DATA_PATH2](https://user-images.githubusercontent.com/76559418/103100969-8e18fa00-4658-11eb-8c29-fc1bc4dc62a5.JPG)
    
3. 상단 메뉴에서 런타임 -> 런타임 유형 -> 하드웨어 가속기 -> GPU로 변경 후 저장 합니다.

4. 런타임 -> 모두실행을 통하여 소스를 실행 합니다.

5. 드라이브 마운트를 위하여 결과 창에 링크가 보이면 해당 링크에 접속 하면 키를 복사 할 수 있습니다.   
   키를 복사 한 후 결과창에 붙여 넣으면 마운트가 됩니다.
