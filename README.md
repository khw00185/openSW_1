
컴퓨터 공학부 201912052 김형우 OpenSW실습
<hr>

<h3>1. Mask_RCNN 공식 Github</h3>
Github https://github.com/matterport/Mask_RCNN에서 git clone

<hr>

<h3>2. 가상환경 설정(python3.7)</h3>
    - tensorflow1.15.5
    - keras2.1.2
    - scikit-image0.16.2
    - protobuf==3.20.*

    이렇게 설치 후 requirements.txt에서 tensorflow, keras, sciket-image를 삭제 후
   - pip install -r requirements.txt
   - python setup.py install

   <hr>


<h3>3. train, weight 설치</h3>
    가중치 설치
    https://github.com/matterport/Mask_RCNN/releases/download/v2.1/mask_rcnn_balloon.h5
    https://github.com/matterport/Mask_RCNN/releases/download/v1.0/mask_rcnn_coco.h5
    
    balloon 데이터셋 설치 https://github.com/matterport/Mask_RCNN/releases/download/v2.1/balloon_dataset.zip 

<hr>

<h3>4. 결과</h3>

    ![결과 1](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T140916.png) <br>
    ![결과 2](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T141333.png) <br>
    ![결과 3](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T141530.png) <br>
    

<hr>

<h3>5. Train</h3>
    노트북인 관계로 samples/balloon/balloon.py의 epoch을 1로 줄이고 STEPS_PER_EPOCH = 100에서 STEPS_PER_EPOCH = 10으로 줄인다.
    Mask_RCNN 공식 깃허브에서 제공하는 COCO weight과 balloon_dataset으로 학습시켜 mask_rcnn_ballon.h5 가중치 파일을 생성한다.
        -python samples/balloon/balloon.py train --dataset=balloon_dataset/balloon --weights=coco

<hr>

<h3>6. 결과</h3>
    train해서 logs파일에 얻어진 mask_rcnn_balloon.h5파일을 루트파일에 붙여넣는다.
    아래는 결과이다.

    ![결과 1](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T174925.png) <br>
    ![결과 2](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T175058.png) <br>
    ![결과 3](https://github.com/khw0015/openSW_1/raw/main/samples/balloon/splash_20231126T175727.png) <br>
   
