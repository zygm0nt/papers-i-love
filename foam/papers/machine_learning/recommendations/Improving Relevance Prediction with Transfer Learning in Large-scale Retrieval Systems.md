# Improving Relevance Prediction with Transfer Learning in Large-scale Retrieval Systems

https://openreview.net/pdf?id=SJxPVcSonN

![](../../../attachments/2021-06-07-14-27-31.png)

![](../../../attachments/2021-06-07-14-28-24.png)

## Contributions
![](../../../attachments/2021-06-07-14-29-54.png)

## The problem

![](../../../attachments/2021-06-07-14-54-39.png)

## Adopting the two-tower architecture to multi-task Learning

![](../../../attachments/2021-06-07-14-57-47.png)

## Training schema

1. first train the model for the auxiliary user engagement objective (with cross-entropy loss)
2. having learned the shared representations, fine tune the model for the main relevanve objective (squared loss)
3. (to prevent overfitting) apply stop gradients for the relevance objective on the shared-bottom layers

**For serving** they only need to store and serve the top layer of the two relevance sub-towers to predict the relevance.

## The success of transfert learning...


![](../../../attachments/2021-06-07-15-07-18.png)


## Follow ups

Other ways of transfer learning:
* mixture of experts, 
* gating

