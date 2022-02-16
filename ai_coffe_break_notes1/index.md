# AI_coffe_break_notes1

<!--more-->

# How to check if a neural network has learned a specific phenomenon?


## Question:
How do we check if a neural network trained on task A has learned a phenomenon specific to task B?

To NLP, the task is called probing/diagnostic classifier/probing task.

## How do we do probing?

- Freeze the parameters of Input layer and Hidden layers,
- Replace the last layers to Probing layers,
- Train the Probing layers on a small dataset.

If task A is Masked word prediction and task B is Sentiment analysis, then:

![P1](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5df6dc63-63cc-4873-adec-ddf1076b300c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220216%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220216T090324Z&X-Amz-Expires=86400&X-Amz-Signature=6fe18308de17d6a2a8c16df96e533dd9c91b91f8f177c9856780b05fa65199b5&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
![P2](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4f234ed6-d104-493c-8f2d-9e90f51af6b3/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220216%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220216T090707Z&X-Amz-Expires=86400&X-Amz-Signature=89b42fec63183d25875fd7b15ced3a0def66223546e932b7973b96ec31738a58&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
![P3](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/eb24d33e-489a-4695-9ce9-af3f826d5181/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220216%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220216T090754Z&X-Amz-Expires=86400&X-Amz-Signature=798c39a05ca4e3de4a88a3ad16a18381f3133e3eb16fbf871b1659ed042b1e1f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## Most recently research

- paper: [Information-Theoretic Probing with Minimum Description Length on](https://arxiv.org/pdf/2003.12298.pdf)

## More info

- Link: https://www.youtube.com/watch?v=fL22NAtMNYo
