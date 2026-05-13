# modele+notebook

# Facial Emotion Recognition - Android
## Lucrare de licență - Mindroc Robert-Andrei, ETTI UPB 2026

## Descriere
Recunoașterea facială a emoțiilor utilizând rețele neuronale convoluționale 
deep-learning de complexitate redusă, cu integrare în platforme Android 
folosind formatul LiteRT (TFLite).

## Baze de date utilizate
- FER-2013 (varianta originală și augmentată)
- RAF-DB
- CK+

## Structura notebook-urilor

### FER-2013 Augmented
- `mobilenet_gpu_fer_augmented.ipynb`
- `vcnn_gpu_fer_2013_augmented.ipynb`
- `vcnn_tpu_fer_2013_augmented.ipynb`
- `vrescnn_fer_augmented_gpu.ipynb`
- `vrescnn_tpu_fer_2023_augmented.ipynb`
- `efficientnet_fer_augmented_tpu.ipynb`

### FER-2013 Original
- `vcnn_gpu_fer_original.ipynb`
- `vcnn_tpu.ipynb`
- `vrescnn_tpu.ipynb`

### RAF-DB
- `notebook_rafdb_gpu.ipynb`

### CK+
- `notebook_ckplus_gpu.ipynb`

### Conversie LiteRT
- `conversie_android_tflite.ipynb`

## Modele finale selectate
| Model | Bază de date | Acuratețe |
|---|---|---|
| MobileNet | FER-2013 aug | 80.91% |
| V-CNN | CK+ | 90.54% |
| V-CNN | FER-2013 orig | 59.96% |
| VRES-CNN | RAF-DB | 76.08% |
