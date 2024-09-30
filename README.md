# AI-Lightbox
Desktop AI based product lightbox tool that will take an image, mask it, and place the product found inside a new product photo. Windows, Linux, macOS.

Features include automatically masking an image, accepting a text description, and generating up to four images of the auto masked product using the text and negative prompt, and storing the history of previous AI lightbox work. 
Additionally, it includes an API X-Ray tab so you can easily how the interaction with the API server works.

The AI Lightbox Desktop client is a powerful UI for automatically masking and generating product images using Stable Diffusion. Also contains an option which takes an OpenAI API key and enhances the prompt using AI. The model source code is not available so use the OpenAI API key functionality at your own risk (use a seperate key for this and revoke it when not using it).

Built with Delphi using the FireMonkey [cross-platform development](https://www.embarcadero.com/products/delphi/) framework this client works on Windows, macOS, and Linux (and maybe Android+iOS) with a single codebase and single UI. At the moment it is specifically set up for Windows.

It also features a REST integration with Replicate.com for providing Generate Image functionality within the client. You need to sign up for an API key to access that functionality. Replicate models can be run in the cloud or locally via docker.

```
docker run -d -p 5000:5000 --gpus=all r8.im/logerzhu/ad-inpaint@sha256:b1c17d148455c1fda435ababe9ab1e03bc0d917cc3cf4251916f22c45c83c7df
curl http://localhost:5000/predictions -X POST \
-d '{"input": {
  "image_path": "https://url/to/file",
    "product_size": "...",
    "prompt": "...",
    "negative_prompt": "...",
    "api_key": "...",
    "pixel": "...",
    "scale": "...",
    "image_num": "...",
    "guidance_scale": "...",
    "num_inference_steps": "...",
    "manual_seed": "..."
  }}'
```

# AI Lightbox Desktop client Screeshot on Windows
![AI Lightbox Desktop client on Windows](/screenshot.png)


