
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

![splash_20231126T140916](https://github.com/khw00185/openSW_1/assets/42068509/066b0899-4e75-41e6-8ca4-82cba7ce59d7)
![splash_20231126T141333](https://github.com/khw00185/openSW_1/assets/42068509/530e97d2-4294-42a7-80ca-9031f0c9c8aa)
![splash_20231126T141530](https://github.com/khw00185/openSW_1/assets/42068509/f7069fac-f942-4c23-be49-5889684e987c)
    

<hr>

<h3>5. Train</h3>
    노트북인 관계로 samples/balloon/balloon.py의 epoch을 1로 줄이고 STEPS_PER_EPOCH = 100에서 STEPS_PER_EPOCH = 10으로 줄인다.
    Mask_RCNN 공식 깃허브에서 제공하는 COCO weight과 balloon_dataset으로 학습시켜 mask_rcnn_ballon.h5 가중치 파일을 생성한다.
        -python samples/balloon/balloon.py train --dataset=balloon_dataset/balloon --weights=coco


<hr>

<h3>6. 결과</h3>
    train해서 logs파일에 얻어진 mask_rcnn_balloon.h5파일을 루트파일에 붙여넣는다.
    아래는 결과이다.

![splash_20231126T174925](https://github.com/khw00185/openSW_1/assets/42068509/a660e07a-82d3-4c79-b5d4-81816f06b1b1)
![splash_20231126T175058](https://github.com/khw00185/openSW_1/assets/42068509/dd00791f-18ee-4858-ad83-a7171182ebba)
![splash_20231126T175727](https://github.com/khw00185/openSW_1/assets/42068509/2e875f99-b3c7-48e3-b21e-165cdde50408)

