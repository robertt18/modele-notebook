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

## Structură

```
CKPLUS/
├── EfficientNet/
│   ├── imagini_rezultate/ la fel pentru toate arhitecturile
│   │   ├── raportul de performanţă după antrenare
│   │   ├── matricea de confuzie + raportul de clasificare detaliat
│   │   ├── graficele pentru evoluţia acurateţii şi scăderea erorii
│   │   └── testarea unei imagini din setul de test
│   └── model.keras
├── MobileNet/
│   ├── imagini_rezultate/
│   └── model.keras
├── VCNN/
│   ├── imagini_rezultate/
│   └── model.keras
├── VRESCNN/
│   ├── imagini_rezultate/
│   └── model.keras
└── notebook_CKPLUS_gpu

FER_2013_original_si_augmented/
├── EfficientNet/
│   └── EfficentNet_gpu/
│       └── fer_2013_augmented
│            ├── model .keras
|            └── notebook_efficientnet_gpu
├── MobileNet_GPU/
│   └── fer_2013_augmented/
│       ├── model.keras
│       └── notebook_mobilenet_gpu
├── VCNN/
│   ├── vcnn_gpu/
│   │   └── fer_2013_augmented/
|   |        ├── model .keras
|   |        └── notebook_vcnn_fer_agumented_gpu
│   │   └── fer_2013_original/
|   |         ├── model .keras
|   |         └── notebook_vcnn_fer_original_gpu
│   └── vcnn_tpu/
│       ├── fer_2013_augmented/
|       |    ├── model .keras
|       |    └── notebook_vcnn_tpu_fer_augmented
│       └── fer_2013_original/
|            ├── model .keras
|            └── notebook_vcnn_tpu_fer_original
└── VRESCNN/
      ├── Vrescnn_gpu/
      │   ├── model .keras
      |   └── notebook_vrescnn_fer_augmented_gpu
      └──vrescnn_tpu/
           ├──fer_2013_augmented
           |    ├── notebook vrescnn_fer_augmented_tpu
           |    └── model .keras
           └──fer_2013_original
                ├── model .keras
                └── notebook_vrescnn_fer_original_tpu
RAF_DB/
├── MobileNet/
│   ├── imagini_rezultate/
│   └── model.keras
├── VCNN/
│   ├── gpu
│       ├── imagini_rezultate/
│       └── model.keras
│   ├── tpu
│       ├── imagini_rezultate/
|       ├── notebook - raf_db_tpu
│       └── model.keras
├── VRESCNN/
│   ├── imagini_rezultate/
│   └── model.keras
└── notebook_Raf_DB_GPU

Tabel excel comparatii global
```
  
## Toate modelele antrenate

| Arhitectură | Dataset | Accelerator | Acuratețe | Timp antrenare | Parametri | Latență |
|---|---|---|---|---|---|---|
| V-CNN | FER-2013 original | GPU | 59.96% | 44.63 min | 1.589.063 | 5.41 ms |
| V-CNN | FER-2013 original | TPU | 57.35% | 6.65 min | 555.719 | 0.69 ms |
| V-CNN | FER-2013 augmented | GPU | 75.54% | 35.62 min | 1.589.063 | 4.72 ms |
| V-CNN | FER-2013 augmented | TPU | 70.42% | 3.41 min | 555.719 | 0.55 ms |
| V-CNN | CK+ | GPU | 90.54% | 1.35 min | 1.589.063 | 6.49 ms |
| V-CNN | RAF-DB | GPU | 74.15% | 23.82 min | 1.589.063 | 5.90 ms |
| V-CNN | RAF-DB | TPU | 63.47% | 4.03 min | 555.719 | 0.65 ms |
| VRES-CNN | FER-2013 original | TPU | 56.09% | 8.96 min | 345.424 | 1.50 ms |
| VRES-CNN | FER-2013 augmented | TPU | 62.77% | 7.05 min | 345.424 | 1.22 ms |
| VRES-CNN | FER-2013 augmented | GPU | 77.82% | 47 min | 345.424 | 6.50 ms |
| VRES-CNN | CK+ | GPU | 89.96% | 2.37 min | 345.424 | 24.34 ms |
| VRES-CNN | RAF-DB | GPU | 76.08% | 24.02 min | 345.424 | 3.64 ms |
| MobileNet | FER-2013 augmented | GPU | 80.94% | 42.93 min | 3.493.063 | 4.11 ms |
| MobileNet | CK+ | GPU | 73.65% | 2.93 min | 3.493.063 | 13.18 ms |
| MobileNet | RAF-DB | GPU | 71.25% | 29.45 min | 3.493.063 | 2.30 ms |
| EfficientNet | FER-2013 augmented | GPU | 79.54% | 52.08 min | 4.058.541 | 4.76 ms |
| EfficientNet | CK+ | GPU | 60.14% | 3.83 min | 4.058.541 | 33.42 ms |
