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




- 3-12 EOF에 대해 알아보기
문제를 보자마자 든 생각은?? 에..? 어캐해? ㅋㅋㅎ
약간 뇌정지왔었음
근데 문제 설명에 적혀있는 **EOF** 에 대해 알아보기로 함

EOF는 end of file의 축약형태이다.  
그리고 EOFError가 있는데 이거는 입력의 끝에 도달했을 때 나는 오류로 try-except으로 해결할 수 있다!
이를 예외처리라 하며 백준은 나한테 이걸 원한것 같다  

try - except 구문 쓰기는 생각보다 간단하다.

```python
try:
  num = int(input()) #try 구문안에 정상적으로 실행됐을 때의 코드 삽입
  print(num + 1)
except:
  print("예외가 발생함") #예외가 발생했을 때 처리할 코드 삽입
```
이런 형식으로 쓰는 데 쉬워서 다행이다라고 생각함.








- 4-1 배열
*이젠 풀려면 배워야하는 구만..ㅋㅋㅋ*  
배열?? array에 대해 배워보겠당  
배열은 리스트 *배우긴 했지만 쓰진 않아서 다 까먹으뮤ㅠ*

리스트 함수
```python
arrays1 = [0,1,2,3,4,5,6]
print(arrays[:]) #[]을 통해서 리스트 일부를 꺼낼 수 있음
print(len(arrays1)) #len()는 괄호안 리스트 요소의 개수를 반환함
for i in range(arrays1):
  print(i) #모든 요소를 루프함
```

<img width="1462" height="974" alt="image" src="https://github.com/user-attachments/assets/60a3a825-c34d-4689-91e0-6148acc50301" />  

list로 입력받고 싶다면!!
```python
U_input = list(map(int, input().split()))
```


- 4-2 리스트 컴프리헨션
*오늘 헷갈리는 거 만ㄴ힝배운다..ㅋㅋㅎ*

```python
list = [표현식 for 변수 in 기존 리스트 if 조건] #=> 이거를 리스트 컴프리헨션이라 함!
```

이를 for 문으로 바꾸면!  

```python
list = []
for 변수 in 기존 리스트:
  if 조건:
    list.append(표현식)
```



