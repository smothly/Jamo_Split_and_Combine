# Jamo_Split_and_Combine
### 한글 자모 분리 결합코드입니다. 기존코드를 응용하여 만들었습니다.
### 출처 : https://github.com/bluedisk/hangul-toolkit
## 주요 변화
### 기존코드의 종성 없을 경우 무시하는 현상
### 완전한 한글이 아닐경우 에러날리는 현상 ex) "ㅋㅋㅋ바1보머어엉청ㅇ" 

.py 파일 다운로드 하셔서
test는
'''
from Jamo_Split import jamo_split, jamo_combine

jamo_split("바보")
jamo_combine("ㅂㅏ_ㅂㅗ_")
'''

# jamo_split
- 한글이 들어올경우 자모 분리
- 영어나 숫자가 나오면 그냥 추가된다.
- end_char 파라미터 추가하여 종성이 없을 경우도 항상 추가
  => 1글자가 무조건 초성/중성/종성으로 분리되어 자모 임베딩할 때 편하다.
  => ex) 바보 -> ㅂㅏ_ㅂㅗ_

# jamo_combine
- jamo_split으로 분리되는 코드를 다시 한글로 합쳐주는 과정이다.
- 자모만 들어올 경우나 한글 외 다른 문자들이 들어와도 합쳐주는 과정 but, hard coding....
  => ㅋㅋㅂㅏ_ㅂㅗ_1abc -> ㅋㅋ바보1abc
