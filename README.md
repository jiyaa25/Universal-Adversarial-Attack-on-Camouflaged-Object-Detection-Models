# Universal-Adversarial-Attack-on-Camouflaged-Object-Detection-Models


## Overview
This project investigates the vulnerability of Camouflaged Object Detection (COD) models to adversarial attacks. We implement a universal adversarial perturbation on a pretrained PNet model.

Instead of generating noise for each image, a single perturbation is learned and applied across multiple inputs. Although visually subtle, this perturbation significantly degrades segmentation performance and often suppresses object detection entirely.

---

## Key Idea
- Learn one universal noise (δ)
- Apply it to all images
- Disrupt the model’s segmentation output

---

## Results
- Clean Output: Accurate segmentation  
- After Attack: Near-zero or suppressed masks  
- Significant drop in performance metrics  

---

## Insights
- COD models are highly sensitive to small perturbations  
- The attack generalizes across multiple images  
- The model relies on fragile feature representations  

---

## Limitations
- White-box setting (requires access to model parameters)  
- Evaluated on a single model (PNet)  
- No defense mechanisms implemented  

---

## Reference Repository
This project uses pretrained weights and dataset structure from:  
https://github.com/zhangjinCV/Noisy-COD

---

## Conclusion
The results show that a single universal perturbation can significantly degrade COD model performance. This highlights the need for developing more robust and reliable models for real-world applications.
