# Computer Vision Project : Multi-class Object Detection using Transfer Learning (Stanford Dogs Dataset)

[FR]

Ce projet étudie la détection multi-classes fine-grained sur le Stanford Dogs Dataset. L’objectif est de détecter et classifier plusieurs races de chiens dans des images en adaptant un modèle Faster R-CNN pré-entraîné. En effet, ce modèle pré-entraîné (sur COCO) est capable de détecter et classifier des objets généraux (chiens, personnes, voitures, camions, etc.), mais il ne peut pas distinguer des races spécifiques de chiens.

Le modèle est affiné (fine-tuned) en ne dégelant que la quatrième couche du backbone ainsi que les ROI heads, ce qui réduit significativement le temps d'entraînement. Ainsi, l’entraînement complet n'a duré qu'une dizaine de dix minutes. Bien que les performances puissent être améliorées grâce à davantage de data augmentation, la configuration actuelle fournit déjà des résultats satisfaisants et démontre l’efficacité d’un fine-tuning partiel.

Les performances sont évaluées à l’aide de métriques de type COCO, notamment la mean Average Precision (mAP) calculée sur plusieurs seuils d’IoU. Enfin, l’inspection visuelle confirme un positionnement précis des bounding boxes ainsi qu’une grande précision de classification sur la majorité des images de test.

[EN]

This project investigates fine-grained multi-class object detection on the Stanford Dogs Dataset. The objective is to detect and classify multiple dog breeds within images by adapting a pre-trained Faster R-CNN model. Indeed, this pretrained model (on COCO) can detect and classify general objects (dogs, people, cars, trucks, etc.), but cannot distinguish specific breeds of dogs.

The model is fine-tuned by unfreezing only the fourth layer of the backbone and the ROI heads, which significantly reduces computational cost. As a result, the full training process required only about ten minutes. Although the model could potentially be further improved through data augmentation, but it already provides satisfactory results and demonstrates the efficiency of partial fine-tuning.

Performance is evaluated using COCO-style metrics, including mean Average Precision (mAP) across multiple IoU thresholds. Finally, visual inspection confirms accurate bounding box placement and high classification accuracy on test samples.
