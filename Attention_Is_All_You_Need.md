요즘 많은 자연어 처리 방법: RNN, LSTM
대부분 RNN을 많이 사용
RNN의 특징
- RNN의 경우 순차적으로 진행함에 있어서 해당 순차적 특성은 유지, but 데이터 거리간의
거리가 멀수록 전부 손실하는 제약(i.e., long-term dependency problem)을 가짐 
- 순차적인 특성 때문에 병렬처리를 할 수 없고, 계산 속도가 느림

=> 이래서 나온 모델
Attention 모델 (데이터간의 거리때문에 데이터가 손실되는 것 때문에 나온 모델)
Transformer: Attention만을 사용한 모델로, 해서 상대적으로, 연산량이 줄고 성능도 매우 높음

Model Architecture
(1) 인코더
총 6개의 레이어
모든 레이어는 같은 서브 레이어
서브 레이어는 총 2개의 레이어를 지님
인코더의 인풋 아웃풋은 512의 디멘션
multi-head attention: 
	Selected Dot-Product Attention
adding residual connection : 이전의 정보가 없어지는걸 방지하기 위해

(2) 디코더
self attention을 사용하는 이유:
1. 레이어당 전체 연산량이 줄어듬
2. 병렬화가 가능한 연산이 늘어남
3. Long-range의 term들의dependency도 잘 학습할 수 있게 된다
4. Attention을 사용하면 모델 자체의 동작을 해석하기 쉬워짐










