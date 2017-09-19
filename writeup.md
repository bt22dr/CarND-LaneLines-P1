# **도로에서 차선 찾기** 

**도로에서 차선 찾기**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

[image0]: ./examples/0.png "Original"
[image1]: ./examples/1.png "Grayscale"
[image2]: ./examples/2.png "Edge"
[image3]: ./examples/3.png "Interest_Region"
[image4]: ./examples/4.png "Interest"
[image5]: ./examples/5.png "Line"
[image6]: ./examples/6.png "Result"

---

### 1. 파이프라인 소개

차선을 추출하기 위한 파이프라인은 6 단계로 구성된다.  
![alt text][image0]  
위와 같은 원본 이미지를 grayscale로 변환한 후  
![alt text][image1]  
canny edge 알고리즘을 수행한다.  
![alt text][image2]  
차선에 해당하는 관심 영역만 잘라낸 후  
![alt text][image4]  
hough 변환을 이용해 직선을 추출해낸다.  
![alt text][image5]  
최종 결과 이미지는 아래와 같다.  
![alt text][image6]  


### 2. 이 방법의 단점

각 단계별로 많은 파라미터들이 사용되는데 입력 이미지의 상태에 따라 적절한 파라미터 값이 달라질 수 있기 때문에 어떤 경우에도 잘 동작하는 강인한 파이프라인으로 사용하기에는 힘들다.


