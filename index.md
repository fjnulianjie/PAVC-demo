<style>
audio{
	height: 50px;
	width: 180px;
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

* first sentence: "Since then physicists have found that it is not reflection, but refraction by the raindrops which causes the rainbows."
* second sentence: "Others have tried to explain the phenomenon physically."

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p227_019.wav" controls preload></audio> | <audio src="audios/target/p313_397.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/adainvc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/autovc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/vqvc/m2f/p227_0192p313_397.wav" controls preload></audio> | <audio src="audios/againvc/m2f/p227_0192p313_397.wav" controls preload></audio> | 
| <audio src="audios/source/p347_017.wav" controls preload></audio> | <audio src="audios/target/p323_122.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2f/p347_0172p323_122.wav" controls preload></audio> | <audio src="audios/adainvc/m2f/p347_0172p323_122.wav" controls preload></audio> | <audio src="audios/autovc/m2f/p347_0172p323_122.wav" controls preload></audio> | <audio src="audios/vqvc/m2f/p347_0172p323_122.wav" controls preload></audio> | <audio src="audios/againvc/m2f/p347_0172p323_122.wav" controls preload></audio> | 

---

#### male-to-male

* first sentence: "The actual primary rainbow observed is said to be the effect of super-imposition of a number of bows."
* second sentence: "The sisters also became the top two players in the world."

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p260_022.wav" controls preload></audio> | <audio src="audios/target/p376_027.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2m/p260_0222p376_027.wav" controls preload></audio> | <audio src="audios/adainvc/m2m/p260_0222p376_027.wav" controls preload></audio> | <audio src="audios/autovc/m2m/p260_0222p376_027.wav" controls preload></audio> | <audio src="audios/vqvc/m2m/p260_0222p376_027.wav" controls preload></audio> | <audio src="audios/againvc/m2m/p260_0222p376_027.wav" controls preload></audio> |
| <audio src="audios/source/p376_199.wav" controls preload></audio> | <audio src="audios/target/p302_114.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2m/p376_1992p302_114.wav" controls preload></audio> | <audio src="audios/adainvc/m2m/p376_1992p302_144.wav" controls preload></audio> | <audio src="audios/autovc/m2m/p376_1992p302_144.wav" controls preload></audio> | <audio src="audios/vqvc/m2m/p376_1992p302_144.wav" controls preload></audio> | <audio src="audios/againvc/m2m/p376_1992p302_144.wav" controls preload></audio> |


---

#### female-to-male

* first sentence: "The difference in the rainbow depends considerably upon the size of the drops, and the width of the colored band increases as the size of the drops increases."
* second sentence: "To the Hebrews it was a token that there would be no more universal floods. "

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p239_021.wav" controls preload></audio> | <audio src="audios/target/p241_187.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/adainvc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/autovc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/vqvc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/againvc/f2m/p239_0212p241_187.wav" controls preload></audio> |
| <audio src="audios/source/p262_014.wav" controls preload></audio> | <audio src="audios/target/p347_120.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/adainvc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/autovc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/vqvc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/againvc/f2m/p262_0142p347_120.wav" controls preload></audio> |

---
