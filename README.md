# 『시작하세요! 텐서플로 2.0 프로그래밍』 예제 코드

기초 이론부터 실전 예제까지 한번에 끝내는 머신러닝, 딥러닝 핵심 가이드

예제 파일 깃허브 저장소입니다.

![](<https://raw.githubusercontent.com/wikibook/tf2/master/tf2_book.jpg>)

[출판사 페이지 링크](<https://wikibook.co.kr/tf2/>)



## 설치법

예제 코드를 다운받은 후 압축을 해제한 폴더에서 아래 명령으로 필요 라이브러리를 설치 후 주피터 노트북에서 실행합니다.

```
pip install -r requirements.txt
```



## 주요 수정 사항

- [2020.02.01] 257p. 예제 8.8에서 캐글에서 데이터세트를 받아오는 부분이 캐글측의 데이터 구조 변경으로 수정되었습니다. [구글 코랩](<https://drive.google.com/open?id=1mj7xE2W5BSMRqbdhdAYHFX-6qgqIQbxV>), [깃허브](<https://github.com/wikibook/tf2/blob/master/Chapter8.ipynb>)

- [2020.04.08] 263p. 예제 8.16의 OOM(Out Of Memory) 발생 문제. 구글 코랩이 [유료 버전](<https://colab.research.google.com/signup>)을 런칭하면서 대용량 RAM 모드를 무료 버전에서 지원하지 않기 때문에 발생한 문제입니다. 해당 부분을 수정한 노트북 파일을 [코랩](https://colab.research.google.com/drive/1oA-qEqoYr-NA4jxQ4SneTPv6NJffEzXQ)과 [깃허브](https://github.com/wikibook/tf2/blob/master/Chapter8_20200408%EC%88%98%EC%A0%95.ipynb)에 올려놓았습니다.


## 주의 사항

- [2020.05.30] 현재 텐서플로 최신 버전에서 model.fit(), model.predict() 함수의 실행 속도가 느린 문제가 있습니다. 10장 강화학습에서는 한 게임에 몇백 번의 model.predict() 함수를 실행하기 때문에 속도가 문제가 될 수 있습니다. 텐서플로 임포트 후 즉시 실행 모드(eager execution)를 비활성화하면 일단 문제를 해결할 수 있습니다. 텐서플로 측에서 문제를 고치면 해당 내용을 삭제하도록 하겠습니다.
```
import tensorflow as tf
tf.compat.v1.disable_eager_execution()
```
[관련 버그 이슈 링크](<https://github.com/tensorflow/tensorflow/issues/32104>)


## 기타

[구글 코랩](<http://bit.ly/2YqzK5E>)에서도 예제 파일을 이용하실 수 있습니다.

버그, 개선 의견은 이슈(Issues)에 남겨주세요.

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fwikibook%2Ftf2)](https://hits.seeyoufarm.com)
