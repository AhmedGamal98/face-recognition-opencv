# Face Recognition with OpenCV

> Real-time face recognition from a webcam using Haar-cascade detection and an LBPH face recognizer.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## How it works

The notebook `face_recognition_webcam.ipynb` runs three steps:

1. **Collect faces:** open the webcam, detect the face with `haarcascade_frontalface_default.xml`, and save grayscale face crops to `dataset/User.<id>.<n>.jpg`.
2. **Train:** train an OpenCV **LBPH** (Local Binary Patterns Histograms) recognizer on the saved faces and write the model to `trainer/trainer.yml`.
3. **Recognize:** run live recognition on the webcam stream and label each detected face.

## Run it

```bash
pip install opencv-contrib-python numpy pillow jupyter
jupyter notebook face_recognition_webcam.ipynb
```

`opencv-contrib-python` is needed for `cv2.face.LBPHFaceRecognizer_create()`.

The face images and the trained model are personal data, so they are not included. Run step 1 to capture your own faces. `dataset/` and `trainer/` are git-ignored.

## Author

**Ahmed Gamal Saber**, Full-Stack Web Developer & AI Engineer
[LinkedIn](https://linkedin.com/in/ahmed-gamal-saber-382081169) · [GitHub](https://github.com/AhmedGamal98)
