자바의 Jframe 과 비슷한 느낌으로 파이썬에도 다양한 모듈이  존재한다.  
turtle,pygame등 과 같이 게임제작에 더 유용한 모듈도 있지만, 이번에는 Tkinter를 사용하였다.

게임은 어렸을 적에 즐겨했지만 몇 년전 서비스를 종료해 이제는 즐길 수 없는  
수 많은 큐플레이 게임 중 햄버거 게임을 구현해보았다.

[##_Image|kage@q1vVG/btq8RTlwwNB/7XyOdCSaDYt5se2RyGRknk/img.gif|alignLeft|data-origin-width="540" data-origin-height="405" data-filename="749070_1524682043.gif" width="551" height="413" data-ke-mobilestyle="widthOrigin"|큐플레이의 햄버거 게임||_##][##_Image|kage@wUgdT/btq8TwQQDS7/K422FRFQMnp2pEi9ZIfx01/img.png|alignLeft|data-origin-width="1127" data-origin-height="790" width="551" height="386" data-ke-mobilestyle="widthOrigin"|내 햄버거 게임||_##]

원작 게임은 푸드트럭 느낌이지만, 재구성하여 포장마차 햄버거 느낌으로 만들었다.

게임 내에 모든 로직과 기능구현들을 직접 짰고,  
웬만한 이미지들도 모두 직접 그려 넣었다. 

## **1.첫화면**

우선 게임을 처음 실행하였을 때 나오는 창은 아래와 같다.

[##_Image|kage@v0RUK/btq8QxXwnho/twqrv2rzXwCiUp51owwgs1/img.png|alignLeft|data-origin-width="1127" data-origin-height="790" width="550" height="385" data-ke-mobilestyle="widthOrigin"|||_##]

햄버거 메뉴 문제를 만들어준 동기들의 메뉴를 선보이며 첫 화면을 구성하였다.

[##_Image|kage@4eA1j/btq8T824Uhl/LhS04nR4MddJejTykpdbtk/img.gif|alignLeft|data-origin-width="600" data-origin-height="401" width="551" height="368" data-ke-mobilestyle="widthOrigin"|시작 화면||_##]

시작 버튼을 누르면 화면이 전환되고 카운트 다운과 함께 게임이 시작된다.

## **2\. 게임 화면**

키보드 방향키를 이용하여 재료를 선택하고 SpaceBar를 눌러 재료를 쌓는다.

[##_Image|kage@bGoLtL/btq8UOi1W7b/ZI1yc5F9Qyzh7ZNt8VEqwk/img.gif|alignLeft|data-origin-width="600" data-origin-height="401" data-filename="맞혔을때.gif" width="549" height="367" data-ke-mobilestyle="widthOrigin"|정답 시||_##]

제한시간은 60초이고 순서대로 재료를 쌓아 정답을 맞히면 정답 표시와 함께  
점수가 올라가고 화면에서 갱신되며, 다음 문제로 넘어간다.  
최고점수는 게임 실행 후 최고점수를 의미한다.

[##_Image|kage@54mlY/btq8TvEuR9g/ldCkRbaEIQYsRa9wveYi80/img.gif|alignLeft|data-origin-width="600" data-origin-height="401" data-filename="틀렸을때.gif" width="549" height="367" data-ke-mobilestyle="widthOrigin"|오답 시||_##]

틀리게 되면 점수는 올라가지 않고,  
정답과 마찬가지로 문제가 바뀌며 만들던 햄버거는 사라진다.

[##_Image|kage@xwQyc/btq8Okkbinp/rJvwUHpwHeEK0rYtgnwfv0/img.gif|alignLeft|width="551" height="368" data-origin-width="600" data-origin-height="401" data-filename="10초.gif" data-ke-mobilestyle="widthOrigin"|제한시간 10초||_##]

제한시간이 10초가 남게되면 타이머가 빨간색으로 변한다.

## **3.게임 종료 및 재시작**

[##_Image|kage@b2EbZU/btq8RsPmVoC/DGMyAfa8ZFf1A7yPDxR8e1/img.gif|alignLeft|data-origin-width="600" data-origin-height="401" data-filename="시간초과.gif" width="549" height="367" data-ke-mobilestyle="widthOrigin"|||_##]

시간이 다 되면 모든 이미지가 지워지고 거대 햄버거가 나타나며 게임은 종료된다.   
Restart버튼을 누르면 카운트와 함께 재시작된다.

[##_Image|kage@baRYGP/btq8KYH1cRZ/zQO3UNSCtxrOnSBARilGU0/img.gif|alignLeft|data-origin-width="600" data-origin-height="401" data-filename="재시작.gif" width="549" height="367" data-ke-mobilestyle="widthOrigin"|재시작||_##]

정답을 맞히거나 틀리거나, 게임 오버가되면 버튼을 눌러도 작동하지 않는다.  
재시작을 하게 되면 현재 점수는 초기화되고 최고점수는 유지되어 다시 갱신을 할 수 있다.

> 코드: [https://github.com/Braveleftji/port/blob/main/Hambuck.py](https://github.com/Braveleftji/port/blob/main/Hambuck.py)
