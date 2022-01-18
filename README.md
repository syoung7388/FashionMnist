# FashionMnist
##
<img src="https://github.com/syoung7388/FashionMnist/blob/main/modeling.PNG" width="70%" height="50%">


#### * Action Function - ReLu [max(0, x)]
#### * Loss Function - NLL [정답O 클래스: -log(a), 정답 X 클래스: -log(1-a)]
#### * Optimizer - Adam 

## 1번 코드의 결과값 
<img src="https://github.com/syoung7388/FashionMnist/blob/main/1_result.PNG" width="40%" height="40%">
training loss는 점차 감소하지만, validation loss 는 널뛰기를 하고 있다. 즉, 현재 overfitting 현상이 일어나고 있다. 

## 해결방법 : Drop Out 
일부 노드들을 훈련에 참여시키지 않고 몇개의 노드를 끊어서, 남은 노드들을 통해서 훈련시키는 방식이다. 이 때 끊어버리는 노드는 랜덤으로 선택한다. pytorch에서는 기본값이 0.5이다. 즉, 절반의 노드를 dropout하고 계산한다. 이렇게 함으로써, training하는 과정에서 oerfitting이 발생하지 않게 할 수 있다. 


<img src="https://github.com/syoung7388/FashionMnist/blob/main/2_result.PNG" width="40%" height="40%">

