## Understading LLM, GPT and Neural Nets From Scratch
This repository contains Jupyter notebooks created while coding along with Andrej Karpathy's `Neural Networks: Zero to Hero` lecture series.  

In a `podcast with Lex Fridman`, He shared how he surprised himself when results for some experiment weren't as he expected and he too learnt something from it while `Going back to basics` in these lectures.

[![Watch on YouTube](andrej.png)](https://www.youtube.com/watch?v=I2ZK3ngNvvI)


Following are covered in the lectures:  
* Backpropagation coded from scratch, `No Autograd`. Intution developed from calculus chain rule and coded in real time
* `Batch normalization` coded and dsicussed in detail
* Neural Net (NN) `training dynamics` discussed in detail
* Importance of weight matrix initialization in NN training
* Activation functions, their graphs and derivates and how they effect NN training
* `Debugging neural net` training issues using various layer level graph plots. (aka Diagnostic tools)
* Explained and developed `Decoder Only Transformer Block` and used it to develop GPT. Also explained Encoder-Decoder attention blocks
* Briefly touched upon post training processes related to LLM (GPT here)

## My Appraoch
As opposed to just watching the lectures and taking handwritten notes, I actively coded along with them. This made me think deeply on what was being taught.  

My notebooks here are slightly different from the lectures in following ways:
* I have intentionally `retained experimental cells`, which he used for explaining concepts and later deleted to avoid clutter, so that it easier to understand later on.
* I have noted `important comments` made by him while explaining some concepts

## Brainstorming with ChatGPT
While watching the lectures, I had many doubts and concerns about various comments and concepts introduced by Andrej. To make better sense of them, I engaged in `deep discussion sessions with ChatGPT`, which turned out to be highly insightful and significantly improved my understanding of the lecture content  

I have shared the snapshots of those chats below as future reference for myself or anyone who may find them useful (visible on expanding through).

<details>
<summary>Why would I have low learning rate for layers close to input when gradient is already low there ?</summary>

**Question Motivation**:
- Without alternate explanation, basic intution should tell you learning rate should compensate for low gradient in initial layers due to cascaded multilication, intentionally wanting it to be low for early layers needs better explanation

![Chat Snapshot 1](chat_gpt_brainstorming/low_lr_for_early_layers_1.jpg)

![Chat Snapshot 1](chat_gpt_brainstorming/low%20lr%20for%20early%20layers%202.jpg)

![Chat Snapshot 1](chat_gpt_brainstorming/low%20lr%20for%20early%20layers%203.jpg)

</details>

<details>
<summary>Should we vary learning rate depending on state of the network, layer position and whether we are training from scratch or not ?</summary>

![Chat Snapshot 1](chat_gpt_brainstorming/lr_schedule_1.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/lr_schedule_2.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/lr_schedule_3.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/lr_schedule_4.jpg)c
</details>

---

Andrej spent considerable time on training dynamics of neural networks and daignostic tools for detecting, debugging issues with neural network training using various graph plots of several quantities.

![Chat Snapshot 1](chat_gpt_brainstorming/traning_dynamic_1.png)
![Chat Snapshot 1](chat_gpt_brainstorming/traning_dynamic_3.png)
![Chat Snapshot 1](chat_gpt_brainstorming/traning_dynamic_4.png)

<details>
<summary>Neural network training dynamics, diagnostic tools and techniques</summary>

![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_5.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_6.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_7.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_9.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_10.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_11.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_12.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_13.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_14.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_15.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_16.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_17.jpg)

</details>

<details>
<summary> Weight, activations and gradient Distribution</summary>

![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_18.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_19.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_20.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_21.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_22.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_24.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_25.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_26.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_27.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_28.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_29.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_30.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_31.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_32.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_33.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_34.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_35.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_36.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_37.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_38.jpg)

</details>

<details>
<summary> We are making distributions to be zero mean normals, so these are small numbers and they will multiply and produce smaller numbers, so how does this make sense, there seems to be opposing forces here</summary>

![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_39.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_40.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_41.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_42.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_43.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_44.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_45.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_46.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_47.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_48.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_49.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_50.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_51.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_52.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_53.jpg)

</details>

<details>
<summary> Is training neural net same as learning from data ?</summary>

![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_54.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_55.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_56.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_57.jpg)
![Chat Snapshot 1](chat_gpt_brainstorming/training_dynamic_58.

</details>


