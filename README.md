## 이전 커밋으로 되돌리기: `git reset`

이전 커밋으로 되돌리기, 다시 되돌아오기. 이미 알고 있는 명령어지만 다시금 학습해본다. 

1. `git reset`  
실제로 사용시에는 `git reset --hard <커밋 이름>`를 사용한다.  
예시를 보도록 하자.
    ```
    vim a.txt # a.txt 만들고 즉시 입력 가능, 'a'라는 행 추가
    git add a.txt
    git commit -m 1
    ...
    vim a. txt # 이후 반복하여 'd'가 입력된 4번째 행까지 추가
    git commit -m 4
    ```
    이후 `git log --oneline`를 하여 커밋 이름을 따고 나서
    ```
    957b5f1 (HEAD -> master) 4
    aa4ad94 3
    293f174 2
    627b11e 1
    ```
    `git reset --hard aa4a`를 해주면 a, b, c 세 행만 있는 파일이 저장된 상태로 돌아간다.  
    원래대로 되돌아가려면  
    `git reset --hard OIRG_HEAD` 를 해주면 된다.
