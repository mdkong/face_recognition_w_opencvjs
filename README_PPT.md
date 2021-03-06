<h1 align="center">Project PT & Demo</h1>  
<br /> 

# λ°ν μμ π₯π₯π₯


```bash
./
βββ λ°ν μμ
β   βββ νλ‘μ νΈ κ°μ λ° κ°λ° λ°°κ²½
β   βββ νλ‘μ νΈ μκ°
β       βββ νλ‘μ νΈ μμΈ μ€λͺ
β       βββ μμ° (Demonstration)
βββ κ°μ  λ°  λ³΄μ μ¬ν­
βββ Q&A
```

<br /> 
<br /> 

# νλ‘μ νΈ κ°μ - Goal  1οΈβ£

- ## Project Title: AI κΈ°μ μ μ΄μ©ν μΌκ΅΄μΈμ νλ‘κ·Έλ¨(μΉμ±) κ°λ°

  - ## Program Name: WAIFRP

  - Web-based AI Face Recognition Program(WebApp)
  - *Pre-Alpha Release through Build, Test and Deployment Automation by MD.Kong*

<br /> 
<br /> 

# νλ‘μ νΈ κ°μ - Objectives 2οΈβ£

- OpenCV.jsλ‘ ML λͺ¨λΈ λΉλ

- ML λͺ¨λΈμ μΉλΈλΌμ°μ λ‘ λ°°ν¬
  - μλ°μ€ν¬λ¦½νΈλ₯Ό μ€νν  μ μλ λͺ¨λ  κ³³μμ κΈ°μ‘΄ λͺ¨λΈ μ€ν

<br /> 
<br /> 

# νλ‘μ νΈ κ°λ° λ°°κ²½ 3οΈβ£

- Python, Flask, MySOL, HTML, CSS etc.μ μ΄μ©ν μΉμλΉμ€λ₯Ό κ°λ° κ³ν
  - OpenCV, JavaScript
- Bootstrap5,  [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) , Github, gh-pages λ±μ μ΄μ©νμ¬ λ°μν μΉμ± κ°λ°λ‘ λ³κ²½
  - OpenCV.js: Webpage, Image Processing, Object Detection, DNN Module etc.
  - All-in-One Github (No need of NPM,Registry, Firebase etc.)

<br /> 
<br /> 

# νλ‘μ νΈ μμΈ μ€λͺ π΅οΈ

## Face Recognition Pipeline
![Face recognition pipeline](https://user-images.githubusercontent.com/77907363/147905111-5c272a23-a312-49c0-9871-e4ccacea8e28.png)


| Pipeline |Network | Comments |
| :------: | ------ |------ |
| 1 | Face Detection | μ΄λ―Έμ§μμ ν κ° μ΄μμ μΌκ΅΄μ κ²μΆ. BGR μ΄λ―Έμ§λ₯Ό μλ ₯ λ°κ³ , μΌκ΅΄μ΄λΌκ³  μκ°ν  μ μλ λΆλΆμ  λ€λͺ¨ λ°μ€λ₯Ό κ·Έλ¦°λ€.  confidenceλ₯Ό μ μ νν΄μΌ νλ€. κ°μ΄ μ»€μ§ μλ‘ μΌκ΅΄ μλ λ€λ₯Έ λμμ΄ ν¬ν¨ λ  κ°λ₯μ±μ΄ λμμ§κ³ , μμμ§λ©΄ μΌκ΅΄ μ νμ΄ μ λ  μλ μλ€ |
| 2 | Feature extraction | μΌκ΅΄ μ΄λ―Έμ§μμ κ°μ₯ μ€μν νΉμ§λ€μ μΆμΆ.  SSD framework (Single Shot MultiBox Detector)μ κΈ°μ΄ν  reduced ResNet-10 model μ¬μ©|
| 3 | Face classification | μΆμΆλ νΉμ§λ€μ κΈ°μ΄νμ¬ μΌκ΅΄ λΆλ₯. μ΄ λ€νΈμν¬λ OpenFaceλΌκ³  λΆλ¦°λ€.  96 x 96 μ¬μ΄μ¦μ RGB μΌκ΅΄ μ΄λ―Έμ§λ₯Ό μλ ₯λ°μ 128μ°¨μμ λ¨μ λ²‘ν°λ₯Ό λ¦¬ν΄νλ©° μ΄λ λ¨μ λ€μ°¨μκ³΅κ°μμμ ν μ μΌλ‘ νκΈ°νλ€.  μ΄λ‘μ¨ λ μΌκ΅΄μ¬μ΄μ μ°¨μ΄λ λ μΆλ ₯λ²‘ν°λ€ μ¬μ΄μ κ±°λ¦¬λ‘ νλ¨ν  μ μλ€([Triplet Loss Function](https://tech.kakaoenterprise.com/63)) |

  - weights: caffemodel.SSD
[res10_300x300_ssd_iter_140000_fp16.caffemodel](https://medium.com/acm-juit/ssd-object-detection-in-real-time-deep-learning-and-caffe-f41e40eea968)

  - Config: [deploy_lowres.prototxt](https://fileinfo.com/extension/caffemodel)
 
  - Recognition Model: [openface.nn4.small2.v1.t7](https://cmusatyalab.github.io/openface/#overview)

<br /> 
<br /> 

## μ½λ© μκ΅¬μ¬ν­ π
- AI κΈ°μ (μΌκ΅΄ μΈμ λ₯λ¬λ λͺ¨λΈ)μ μ΄μ©νμ¬
  - DNN λͺ¨λΈ μ μ  λ° μ€λΉ (Caffemodel, OpenFace etc.)
  
- μΉμμ μ€μκ°μΌλ‘ μΉ΄λ©λΌ μμμ μλ ₯λ°μ κ·Έ μ€μμ μ¬λμ μΌκ΅΄ λΆλΆμ μΆμΆ λ° μ μ₯νκ³  
  - Object Detection, Feature map μμ±
 
- κΈ°μ€(anchor)μ΄ λλ μΌκ΅΄κ³Ό μΌμΉν  κ°λ₯μ±μ΄ λμ μΌκ΅΄μ κ΅¬λ³ν΄ λΈλ€
  - Identification (μλ³), Verification (κ²μ¦)


<br /> 
<br /> 

## κ°λ°μ μ¬μ©λ μμλ€ (π πΆResources)

| Resources | Use | README |
| ------ | ------ |------ |
| Bootstrap | νμ΄μ§ μμ± | [https://getbootstrap.com/docs/5.0/getting-started/introduction/] |
| OpenCV.js | ν΅μ¬ κΈ°λ₯ λͺ¨λ | [https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html] |
| GitHub | Registry, μΉνΈμ€ν & λ°°ν¬ | [https://github.com/mdkong/face_recognition_w_opencvjs#readme] |
| Colab | IDE | [https://colab.research.google.com/] |
| Google Drive | DB | [https://www.google.com/drive/] |


<br /> 
<br /> 

## μ½λ μ°Έμ‘°
  - <https://github.com/mdkong/cv_face_recog/blob/main/index.html>

<br /> 
<br /> 

## μμ ν΄λ λͺ©λ‘

~~~
D:\GITHUB\FACE_RECOGNITION_W_OPENCVJS
+---.github
|   \---workflows
+---assets
|   +---brand
|   \---dist
|       +---css
|       \---js
+---data
\---js
~~~


<br /> 
<br /> 

## νλ‘κ·Έλ¨ λ°λͺ¨
  - <https://mdkong.github.io/face_recog/>

<br /> 

<br /> 

# μΆν λ³΄μ λ΄μ© π οΈ π·

- λ€μν λͺ¨λΈ λ° νλΌλ©ν°λ₯Ό λ³κ²½νλ©΄μ νμ€νΈ ν΄ λ³Ό νμ
  - tensorflow.js model, YOLO etc.
  
- λ€μν κΈ°λ₯μ ν¬ν¨ν Interface κ°μ  λ° νλ©΄ κ΅¬μ±

- μλλ‘μ΄λ νλ«νΌμμμ ν¨ν€μ§ μ²λ¦¬ λ° λ°°ν¬ (νλ μ΄μ€ν μ΄μ λ°°ν¬)
- 3D κΈ°λ₯ κ΅¬νν λΌμ΄λΈλ¬λ¦¬ (WebAR, WebVR λ±) νμ©ν μ± κ°λ°  
  


<br /> 

<br /> 

<br /> 

<br /> 

---  

κ°μ¬ν©λλ€ π

Many Thanks to @github & all the Open Source Maintainers from the bottom of my heart ππ
---

