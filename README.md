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
## Arhitecturi utilizate
VCNN
VRESCNN
MobileNet
EfficientNet

## Modele finale selectate
| Model | Bază de date | Acuratețe |
|---|---|---|
| MobileNet | FER-2013 aug | 80.91% |
| V-CNN | CK+ | 90.54% |
| V-CNN | FER-2013 orig | 59.96% |
| VRES-CNN | RAF-DB | 76.08% |
