# hackathon_project

신경망 : kobert의 hidden_size를 그대로 사용

한정적인 컴퓨팅 파워를 고려하여 효율적으로 학습시키기위해 아래 사항들을 적용

scheduler(get_cosine_schedule_with_warmup )
: 코사인 함수에 의해 정의되는 주기를 따라 learning rate가 최소값과 최대값을 오고가는 기법

AdamW
: Adam의 단점을 보안한 optimizer, 그중 weight값을 고정시켜 bertAdam을 이용하였음

clip_grad_norm_
: 기울기 소실 & 폭주문제를 해결하기 위해 기울기의 절대값이 
특정 값 이상을 넘어가게 될 경우 기울기의 절대값을 줄여주는 간단한 기법
