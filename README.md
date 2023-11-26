컴퓨터 공학부 201912052 김형우 OpenSW실습
<hr>

<h1>1. Mask_RCNN 공식 Github https://github.com/matterport/Mask_RCNN에서 git clone</h1>

<hr>

<h1>2. 가상환경 설정(python3.7)</h1>
    - tensorflow1.15.5
    - keras2.1.2
    - scikit-image0.16.2
    - protobuf==3.20.*

    이렇게 설치 후 requirements.txt에서 tensorflow, keras, sciket-image를 삭제 후
   - pip install -r requirements.txt
   - python setup.py install

   <hr>


<h1>3. train, weight 설치</h1>
    가중치 설치
    https://github.com/matterport/Mask_RCNN/releases/download/v2.1/mask_rcnn_balloon.h5
    https://github.com/matterport/Mask_RCNN/releases/download/v1.0/mask_rcnn_coco.h5
    
    balloon 데이터셋 설치 https://github.com/matterport/Mask_RCNN/releases/download/v2.1/balloon_dataset.zip 

<hr>


<h1>4. 결과</h1>
     <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T140916.png"> <br>
     <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T141333.png"> <br>
     <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T141530.png"> <br>

<hr>

<h1>5. Train</h1>
    노트북인 관계로 samples/balloon/balloon.py의 epoch을 1로 줄이고 STEPS_PER_EPOCH = 100에서 STEPS_PER_EPOCH = 10으로 줄인다.
    Mask_RCNN 공식 깃허브에서 제공하는 COCO weight과 balloon_dataset으로 학습시켜 mask_rcnn_ballon.h5 가중치 파일을 생성한다.
        -python samples/balloon/balloon.py train --dataset=balloon_dataset/balloon --weights=coco

<hr>

<h1>6. 결과</h1>
    train해서 logs파일에 얻어진 mask_rcnn_balloon.h5파일을 루트파일에 붙여넣는다.
    아래는 결과이다.
    <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T174925.png"> <br>
     <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T175058.png"> <br>
     <img width="433" alt="splash" src="https://github.com/khw0015/openSW_1/samples/balloon/splash_20231126T175727.png"> <br>
   
