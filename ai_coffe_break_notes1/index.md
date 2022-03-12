# AI coffe break: notes1

<!--more-->



# How to check if a neural network has learned a specific phenomenon?


## Question:
How do we check if a neural network trained on task A has learned a phenomenon specific to task B?

To NLP, the task is called probing/diagnostic classifier/probing task.

## How do we do probing?

- Freeze the parameters of Input layer and Hidden layers,
- Replace the last layers to Probing layers,
- Train the Probing layers on a small dataset

If task A is Masked word prediction and task B is Sentiment analysis, then:


![P1](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/coffeN1_P1.png)
![P2](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/coffeN1_P2.png)
![P3](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/coffeN1_P3.png)

## Most recently research

- paper: [Information-Theoretic Probing with Minimum Description Length on](https://arxiv.org/pdf/2003.12298.pdf)

## More info

- Link: https://www.youtube.com/watch?v=fL22NAtMNYo
