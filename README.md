# malicious_comment_classification
KoBERT를 사용한 온라인 뉴스 악성 댓글 데이터 이진 분류

(❕자세한 프로젝트 내용과 결과, 회고는 [블로그](https://donghae0230.tistory.com/123)에 작성해두었습니다.)


### 🙋‍♂️사용 데이터
---
편견, 혐오표현, 모욕에 대한 한국어 온라인 뉴스 댓글 데이터 [Korean HateSpeech Dataset](https://github.com/kocohub/korean-hate-speech) 활용

- 총 9,381개의 댓글(훈련 7,896개/검증 417개/테스트 974개)
- 태깅 과정에 대한 [가이드라인](https://www.notion.so/c1ecb7cc52d446cc93d928d172ef8442)
- Deepest 학술그룹 세미나 [발표자료](https://www.slideshare.net/WonIkCho/2005-moon-joydeepestfinal)
    - 온라인 포털 연예 뉴스기사의 경우 두터운 독자층, 확실한 타깃, 특정 집단에 치우치지 않는 갈등 존재
    - 데이터 수집 기간 Jan.2018 - Feb. 2020

데이터셋 중에서도 🌈***Gender-related bias*** 데이터 사용
- 성별에 따른 역할이나 능력에 대한 편견
- 성별과 나이에 대한 편견
- 그 외 특정 성별, 성적 지향성, 성 정체성, 성 관련 사상을 가진 집단에 대한 편견

### 🙋‍♂️사용 모델
---
SK T-Brain [KoBERT](https://github.com/SKTBrain/KoBERT)를 사용한 모델 생성
- [naver_review_classifications_pytorch_kobert](https://colab.research.google.com/github/SKTBrain/KoBERT/blob/master/scripts/NSMC/naver_review_classifications_pytorch_kobert.ipynb#scrollTo=itIExnuLbSap) 코드 참고

> 💡 KoBERT는 BERT base multilingual cased의 한국어 성능 한계를 해결하기 위해 등장

> 💡 BERT는 2018년 구글에서 발표된 기계번역 모델로, 약 33억개의 단어로 pre-training 되어 있으며 사용 목적에 따라 fine-tuning이 가능


