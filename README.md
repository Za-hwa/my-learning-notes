# 백준 정리 노트

## 단계별 풀어보기

- 3-6 빠른 A + B

  
**sys.stdin.readline**
  *아예 처음 보는 코드*  
  백준에서 이거 써라길래 서칭함


  말 그대로 input 대신 쓸 수 있는 것  
  하지만! input 보다 빠르고 효율적 & 많은 입력을 처리할 때 유용함

  ```python  
  import sys  
  number = int(sys.stdin.readline())
  ```
  위의 형식을 따르는데 import sys 필수!

  추가적으로 sys.stdin.readline()을 쓰게 되면 뒤에 개행문자가 포함됨  
  *개행문자는 \n 을 일컫음*  
  그래서 .rstrip()을 뒤에 붙여줌으로써 공백이나 개행문자 등을 제거해서 사용할 수 있음!  
  개행문자가 포함될 시 숫자 변환 및 비교에 오류 발생
