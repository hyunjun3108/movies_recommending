파이썬을 활용한 영화 추천 시스템 구현

1.파이썬으로 협업 필터링을 구현.
행렬분해(Matrix Factorization)을 기반(잠재 요인 협업 필터링, latent factor collaborative filtering)으로 한 추천 시스템을 파이썬으로 구현하였다.

협업 필터링(Collaborative Filtering)
크게 두가지 종류가 있다. 아이템 기반 협업 필터링과 잠재 요인 기반 협업 필터링이 있는데 여기서는 잡재 요인 기반의 협업 필터링을 파이썬으로 구현하였다.

데이터 - kaggle에 있는 movielens 데이터를 사용
이 데이터는 사용자-영화 평점 기반 데이터와 영화 정보 데이터 2가지로 나뉘어져있고, 영화 평점 데이터는 10만개가 넘고, 영화 데이터는 대략 9000여개 정도가 있다.


2. 하지만, 1)의 경우는 특정 영화와 비슷한 영화를 추천해주는 것이지 개인에게 맞춤형으로 추천을 해주는 것이 아니다. 만약 '인셉션' 영화를 input으로 넣으면 비슷한 영화 목록을 알려주는 것이 전부이다.
때문에 2)에서는 사용자 개인 영화 히스토리를 기반으로 영화를 추천해주는 추천 시스템을 구현하였다.
