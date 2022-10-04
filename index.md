<style>
audio{
	height: 50px;
	width: 200px;
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

* first sentence: "Downing Street will make the second appointment in the Scotland Office today."
* second sentence: "There were unconfirmed reports that it was cannabis."

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p246_087.wav" controls preload></audio> | <audio src="audios/target/p230_252.wav" controls preload></audio> | <audio src="audios/TSDFVC/m2f/p246_0872p230_252.wav" controls preload></audio> | <audio src="audios/adainvc/m2f/p246_0872p230_252.wav" controls preload></audio> | <audio src="audios/autovc/m2f/p246_0872p230_252.wav" controls preload></audio> | <audio src="audios/vqvc/m2f/p246_0872p230_252.wav" controls preload></audio> | <audio src="audios/againvc/m2f/p246_0872p230_252.wav" controls preload></audio> | 
| <audio src="audios/source/p298_091.wav" controls preload></audio> | <audio src="audios/target/p257_051.wav" controls preload></audio> | <audio src="audios/TSDFVC/m2f/p298_0912p257_051.wav" controls preload></audio> | <audio src="audios/adainvc/m2f/p298_0912p257_051.wav" controls preload></audio> | <audio src="audios/autovc/m2f/p298_0912p257_051.wav" controls preload></audio> | <audio src="audios/vqvc/m2f/p298_0912p257_051.wav" controls preload></audio> | <audio src="audios/againvc/m2f/p298_0912p257_051.wav" controls preload></audio> | 

---

#### male-to-male

* first sentence: "Their courage, and their honesty, should be respected."
* second sentence: "I've got the same feeling as I had last week in Germany."

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p260_030.wav" controls preload></audio> | <audio src="audios/target/p304_192.wav" controls preload></audio> | <audio src="audios/TSDFVC/m2m/p260_0302p304_192.wav" controls preload></audio> | <audio src="audios/adainvc/m2m/p260_0302p304_192.wav" controls preload></audio> | <audio src="audios/autovc/m2m/p260_0302p304_192.wav" controls preload></audio> | <audio src="audios/vqvc/m2m/p260_0302p304_192.wav" controls preload></audio> | <audio src="audios/againvc/m2m/p260_0302p304_192.wav" controls preload></audio> |
| <audio src="audios/source/p243_027.wav" controls preload></audio> | <audio src="audios/target/p304_018.wav" controls preload></audio> | <audio src="audios/TSDFVC/m2m/p243_0272p304_018.wav" controls preload></audio> | <audio src="audios/adainvc/m2m/p243_0272p304_018.wav" controls preload></audio> | <audio src="audios/autovc/m2m/p243_0272p304_018.wav" controls preload></audio> | <audio src="audios/vqvc/m2m/p243_0272p304_018.wav" controls preload></audio> | <audio src="audios/againvc/m2m/p243_0272p304_018.wav" controls preload></audio> |


---

#### female-to-male

* first sentence: "The difference in the rainbow depends considerably upon the size of the drops, and the width of the colored band increases as the size of the drops increases."
* second sentence: "To the Hebrews it was a token that there would be no more universal floods. "

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p239_021.wav" controls preload></audio> | <audio src="audios/target/p241_187.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/adainvc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/autovc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/vqvc/f2m/p239_0212p241_187.wav" controls preload></audio> | <audio src="audios/againvc/f2m/p239_0212p241_187.wav" controls preload></audio> |
| <audio src="audios/source/p262_014.wav" controls preload></audio> | <audio src="audios/target/p347_120.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/adainvc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/autovc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/vqvc/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/againvc/f2m/p262_0142p347_120.wav" controls preload></audio> |

---

#### female-to-female

* first sentence: "Aristotle thought that the rainbow was caused by reflection of the sun's rays by the rain. "
* second sentence: "We've always had three options, and none of them perfect."

| **Source** | **Target** | **Ours** | **AdaIN-VC** | **AutoVC** | **VQVC+** | **AGAIN-VC** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p262_018.wav" controls preload></audio> | <audio src="audios/target/p340_399.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2f/p262_0182p340_399.wav" controls preload></audio> | <audio src="audios/adainvc/f2f/p262_0182p340_399.wav" controls preload></audio> | <audio src="audios/autovc/f2f/p262_0182p340_399.wav" controls preload></audio> | <audio src="audios/vqvc/f2f/p262_0182p340_399.wav" controls preload></audio> | <audio src="audios/againvc/f2f/p262_0182p340_399.wav" controls preload></audio> |
| <audio src="audios/source/p306_304.wav" controls preload></audio> | <audio src="audios/target/p351_355.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/adainvc/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/autovc/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/vqvc/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/againvc/f2f/p306_3042p351_355.wav" controls preload></audio> |

---

#### Ablation Study

* first sentence: "Others have tried to explain the phenomenon physically."
* second sentence: "The sisters also became the top two players in the world."
* third sentence: "To the Hebrews it was a token that there would be no more universal floods. "
* fourth sentence: "We've always had three options, and none of them perfect."

| **Source** | **Target** | **Ours** | **-PAIN** | **-PANet** |
| :---: | :---: | :---: | :---: | :---: |
| <audio src="audios/source/p347_017.wav" controls preload></audio> | <audio src="audios/target/p323_122.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2f/p347_0172p323_122.wav" controls preload></audio> | <audio src="audios/PAVC-PAIN/m2f/p347_0172p323_122.wav" controls preload></audio> |<audio src="audios/PAVC-PANet/m2f/p347_0172p323_122.wav" controls preload></audio> |
| <audio src="audios/source/p376_199.wav" controls preload></audio> | <audio src="audios/target/p302_114.wav" controls preload></audio> | <audio src="audios/PAVC_128/m2m/p376_1992p302_114.wav" controls preload></audio> | <audio src="audios/PAVC-PAIN/m2m/p376_1992p302_114.wav" controls preload></audio> | <audio src="audios/PAVC-PANet/m2m/p376_1992p302_114.wav" controls preload></audio> |
| <audio src="audios/source/p262_014.wav" controls preload></audio> | <audio src="audios/target/p347_120.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/PAVC-PAIN/f2m/p262_0142p347_120.wav" controls preload></audio> | <audio src="audios/PAVC-PANet/f2m/p262_0142p347_120.wav" controls preload></audio> |
| <audio src="audios/source/p306_304.wav" controls preload></audio> | <audio src="audios/target/p351_355.wav" controls preload></audio> | <audio src="audios/PAVC_128/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/PAVC-PAIN/f2f/p306_3042p351_355.wav" controls preload></audio> | <audio src="audios/PAVC-PANet/f2f/p306_3042p351_355.wav" controls preload></audio> |

---
