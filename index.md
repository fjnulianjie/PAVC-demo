<style>
audio{
	height: 50px;
	width: 100px;
	margin: auto;
}
</style>
- - -
## Abstract
Arbitrary voice conversion, also named as zero-shot voice conversion, is a challenging task which transforms the voice from one speaker and to any another speaker. 
Comparing with traditional one-to-one or many-to-many tasks, it is more difficult and attractive in real-world scenarios. Some previous studies can achieve it, but most of them compress the speaker information of an utterance into a  fixed-length vector. To overcome the such problem, we propose a novel way to obtain a time-varying speaking style embedding by using an attention mechanism.Instead of static and averaged style information, we focus on how to obtain style information which depends on the content information.For that, we design the Phoneme Attention Net (PANet) and the Phoneme Attention Instance Normalization (PAIN), then combined them into our proposed Phoneme Attention Voice Conversion (PAVC) to achieve the style adaptive voice conversion. It can consider the influence of local content information on style distribution without parallel corpus. Experimental results demonstrate that the proposed PAVC outperforms the state-of-the-art approaches on arbitrary voice conversion.
- - -

### Demo Utterances (All of the following speakers were not seen during training)

---

#### male-to-female

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** | **Transcription** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p227_019.wav" controls preload></audio> | <audio src="audios/target/p313_397.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/adainvc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/autovc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/vqvc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/againvc/m2f/p227_0192p313_397.wav" controls preload></audio> | <font size=2>"Since then physicists have found that it is not reflection, but refraction by the raindrops which causes the rainbows."</font> |

---
