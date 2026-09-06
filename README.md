# CS7150-Homework-5

This homework has two notebooks about **reinforcement learning with verifiable rewards (RLVR)**,
the method behind reasoning models such as DeepSeek-R1.  Both use the same algorithm, GRPO.

So far in the course every model has learned by imitation: predict the next token of text that
somebody else wrote.  RLVR is different.  The model writes its own solutions, a program checks
them, and the model is pushed toward the solutions that passed.  There is no demonstration to copy.

- **Homework 5.1 - RLVR from scratch.**  A 100k-parameter transformer learns to add three
  digits.  You write the verifier, the group-relative advantage, and the GRPO loss, then run
  experiments on the KL penalty, a length penalty, and a sloppy verifier that the model learns to
  exploit.  Runs on a laptop CPU in a few minutes.
- **Homework 5.2 - GRPO on a real model.**  Qwen2.5-0.5B-Instruct on GSM8K word problems with the
  `trl` library.  You write the reward functions and evaluate before and after training.
  Needs a GPU; a free Google Colab T4 is enough, but budget about an hour for training.

Do 5.1 first: everything in 5.2 is the same loop at a scale where you cannot see inside it.

Tasks:

1. Complete the TODOs in HW 5.1 and HW 5.2, and answer the written questions in the notebooks.
2. Submit through Canvas: a PDF of each notebook plus a link to your notebook online.
