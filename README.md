# Raspberry-Pi-2-W-Zero-Generative-Art
## Stable Diffusion 1.5
- Stable Diffusion 1.5 is a latent text-to-image diffusion model capable of generating photo-realistic images given any text input. It includes almost 1 billion parameters, so recommended minimum RAM/VRAM is typically 8GB. 
- However, Raspberry Pi Zero 2 W only has 512 MB of RAM. Thus, It is impossible to run Stable Diffsion 1.5 on it.
- To solve this problem, OnnxStream was written.
## OnnxStream
- OnnxStream is based on the idea of decoupling the inference engine from the component responsible of providing the model weights, which is a class derived from WeightsProvider.
- For example a custom WeightsProvider can decide to download its data from an HTTP server directly, without loading or writing anything to disk (hence the word "Stream" in "OnnxStream"). Three default WeightsProviders are available: DiskNoCache, DiskPrefetch and Ram.
- For more information, you can read in this: [OnnxStream](https://github.com/vitoplantamura/OnnxStream.git)
