# DisCo-Speech: Controllable Zero-Shot Speech Generation with A Disentangled Speech Codec

<!-- [![Demo Page](https://img.shields.io/badge/Project-Page-green?style=for-the-badge&logo=googlechrome&logoColor=white)](https://silyfox.github.io/DisCo-Speech/)
[![arXiv](https://img.shields.io/badge/arXiv-Paper-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/xxxx.xxxxx) -->

<div align="center">
    <a href="https://"><img src="https://img.shields.io/badge/Paper-ArXiv-red" alt="paper"></a>
    <a href="https://disco-speech.github.io/DisCo-demo/"><img src="https://img.shields.io/badge/Demo-Page-lightgrey" alt="version"></a>
    <!-- <a href="https://huggingface.co/DisCo-Speech/DisCo-speech"><img src="https://img.shields.io/badge/Hugging%20Face-Model%20Page-yellow" alt="Hugging Face"></a> -->
    <a href="https://github.com/disco-speech/DisCo-Speech-main"><img src="https://img.shields.io/badge/Platform-linux-lightgrey" alt="version"></a>
    <a href="https://github.com/disco-speech/DisCo-Speech-main"><img src="https://img.shields.io/badge/Python-3.12+-orange" alt="version"></a>
    <a href="https://github.com/disco-speech/DisCo-Speech-main"><img src="https://img.shields.io/badge/PyTorch-2.5+-brightgreen" alt="python"></a>
    <!-- <a href="https://github.com/disco-speech/DisCo-Speech-main"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="mit"></a> -->
</div>

## 📝 Abstract
Recent codec-based language models (LMs) have revolutionized text-to-speech (TTS). 
However, since standard codecs tightly couple timbre and prosody, continuation-based LMs inevitably replicate this entanglement, hindering independent control.
Recent efforts attempt to break this entanglement via codec design, but insufficient decoupling remains a critical bottleneck. 
To tackle this challenge, we propose DisCo-Speech, a zero-shot cotrollable TTS framework that enables prosody control and voice cloning via a disentangled speech codec (DisCodec) and an LM-based generator. 
The core component, DisCodec, contains two core stages: 1) Tri-factor disentanglement: using parallel encoders and hybrid correlation-based losses, it explicitly decouples speech into content, prosody, and timbre subspaces; 2) Fusion and reconstruction: given the learned subspaces, DisCodec decoder further fuses content and prosody into unified content-prosody tokens suitable for LM prediction, while jointly optimizing reconstruction quality to resolve the inherent trade-off between disentanglement and reconstruction. 
With this design, the LM performs contextual prosodic continuation from a style prompt while the decoder handles target timbre injection, forming DisCo-Speech's zero-shot control paradigm.

<div align="center">

<br>
<img src="figs/codec.jpg" width="800" alt="DisCo-Speech Codec"/>
Figure 1: The overview of DisCo-Speech.
<img src="figs/tts.jpg" width="800" alt="DisCo-Speech Architecture"/>
Figure 2: The structure and two-stage training of DisCodec.
<br>
</div>

---

## 🎵 Audio Samples
<!-- **The best way to understand our work is to listen to the samples!** -->

### 👉 [Click here to visit our Demo Page](https://disco-speech.github.io/DisCo-demo/) 👈

We provide extensive samples demonstrating:
* DisCo-Speech: Zero-shot Controllable Speech Generation
  * Voice Cloning Comparison With Other Mthods
  * Zero-Shot Controllable generation Comparison With Other Methods
* DisCodec: Disentangled Speech Codec
  * DisCodec Reconstruction Performance
  * Zero-Shot Voice conversion of DisCodec
  * Disentanglement Visual Analysis
* Additional DisCo-Speech Zero-Shot Demos
  * Voice Cloning
  * Zero-Shot Controllable Generation Demos

---

## 📢 News
* **[2025-12-16]** The project page is now live! Check out the samples [here](https://disco-speech.github.io/DisCo-demo/).
* **[2025-12-16]** Our paper is available on arXiv.

> 🚧 **Code Release Status:**
>
> We are actively preparing the source code for release. Currently, the code is undergoing internal review and refactoring to ensuring it is easy to run and reproduce.
>
> Please **Star ⭐** this repository to get the latest updates!

---

## 🗺️ Roadmap

- [x] Launch Project Page (Demo) 🌐
- [x] Release Paper on arXiv 📄
- [ ] Release Inference Code 💻
- [ ] Release Pretrained Models (Checkpoints) 📦
- [ ] Release Training Scripts ⚙️
- [ ] Hugging Face Spaces Demo 🚀

---

<!-- ## 🔗 Citation

If you find **DisCo-Speech** useful for your research, please consider citing our paper:

```bibtex
@article{author202Xdiscospeech,
  title={DisCo-Speech: [Full Title]},
  author={Lastname, Firstname and Lastname, Firstname},
  journal={arXiv preprint arXiv:xxxx.xxxxx},
  year={202X}
} -->