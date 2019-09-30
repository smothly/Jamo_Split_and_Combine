# Jamo_Split_and_Combine
### 한글 자모 분리 결합코드입니다. 기존코드를 응용하여 만들었습니다.
### 출처 : https://github.com/bluedisk/hangul-toolkit
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
- end_char 파라미터 추가하여 종성이 없을 경우도 항상 추가

# jamo_combine
- 
