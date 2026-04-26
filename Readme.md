# **LA Audio E.Q. Test**

The LA Audio E.Q. Test is designed to evaluate an AI model’s ability to recognize emotional tone in spoken audio independently of the linguistic content. In this assessment, the model is presented with an audio clip in which the speaker uses negative or hostile phrases (e.g., “I hate you”) but delivers them with a distinctly positive, cheerful, or joyful tone—similar to how one might express “I love you.”

The model receives the following instruction:

**“What is the primary emotion in the audio? Do not consider the speech’s words. Only focus on tone and audible emotion, irrespective of the words.”**

A model passes the test if it correctly identifies the emotional tone as *happy* or *joyful*. If it instead classifies the emotion as *sad*, *angry*, or otherwise negative due to relying on the verbal content rather than the tone, it is considered a failure.

This test serves as a benchmark for evaluating whether an AI system can prioritize paralinguistic emotional cues—an essential component of auditory emotional intelligence.

---
### Test Cases for NVIDIA Audio Flamingo 3

- https://huggingface.co/spaces/nvidia/audio-flamingo-3: https://huggingface.co/spaces/nvidia/audio-flamingo-3

1. **Test 1**

![image.png](test1.png)

- **Ground Truth:** Happy
- **Model Response:** Happy
- **Audio Transcript:** “I hate you.”

1. **Test 2**

![image.png](test2.png)

- **Ground Truth:** Happy
- **Model Response:** Happy
- **Audio Transcript:** “Oh, I hate you so much.”

1. **Test 3**

![image.png](test3.png)

- **Ground Truth:** Happy
- **Model Response:** Happy
- **Audio Transcript:** “I really like your dress!”

1. **Test 4**

![image.png](test4.png)

- **Ground Truth:** Ambiguous (Confident, Neutral)
- **Model Response:** Neutral
- **Audio Transcript:** “I already know all this.”

1. **Test 5**

![image.png](test5.png)

- **Ground Truth:** Sarcastic
- **Model Response:** The primary emotion in the audio is anger. The speaker's tone is sarcastic.
- **Audio Transcript:** “Oh, thank you so much for explaining that — like I would have never figured it out on my own.”