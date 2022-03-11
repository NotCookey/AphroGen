<h1 align="center">AphroGen</h1>
<h4 align="center">A Fast, Free And Reliable Image Generation API</h4>

**Production Servers**

| Name       | URL                 | Description                                                                                                                                                                                                        |
| :--------- | :------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Production | aphro.vercel.app    | The public API server for generating images                                                                                                                                                                                            |

## API Reference

- [Generate Images](#generate-images)
- [Image Generation Routes](#image-generation-routes)
- [Project Information](#project-information)

## Generate Images

The `/generate` endpoint of the API is used to produce various pictures. The Generate Endpoint is made up of several routes, each with its own goal of generating unique images.

Example

```HTTP
GET /generate/wanted?avatar=https://avatars.githubusercontent.com/u/100358774?s=200&v=4
```
<kbd><img src="https://media.discordapp.net/attachments/930065267848003590/951845033903026296/unknown.png" width=150px></kbd>

The `generate/wanted` route is used to generate a wanted image with the provided avatar image link. Check The API Reference for all different routes, [API Reference](#api-reference). 


It will send you the file as an attachment whenever you request an image. If you're using code to produce, you'll need to use an Image Libary to parse the image raw data from the request's content. Here's an example in Python
```python
import requests
from PIL import Image

data=requests.get("https://aphro.vercel.app/generate/wanted?avatar=https://avatars.githubusercontent.com/u/100358774?s=200&v=4",stream=True).raw
im=Image.open(data)
im.save("wanted.png")
```
The code above requests the API to generate a wanted image with the provided avatar image link and using `.raw` to load the raw content of the requests. Then using [Pillow Libary](https://pypi.org/project/Pillow) to read the Raw Data into an actual image and saving it as `wanted.png`.

## Image Generation Routes

All the routes in this Image Generation Section Requires the Parameter `avatar` or `image` or Either Both In Its URL.

```HTTP
GET /generate/wanted?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/beautiful?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/3000years?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/expose?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/hail?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/deepfuck?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/circle?avatar={AVATAR_IMAGE_LINK}
```
```HTTP
GET /generate/blur?avatar={AVATAR_IMAGE_LINK}
```

This Route Specifically Requires Both The `avatar` and `image` parameter in its URL

```HTTP
GET /generate/batslap?avatar={AVATAR_IMAGE_LINK}&image={SECOND_AVATAR_LINK}
```

## Project Information

Because the API is still in development and will be, small errors in endpoints and routes are to be expected. I still have a lot more things in mind for this API, which I will implement soon.

## Where's The Code?

At the moment, this API is not open-source since I still have a lot of stuff to add, correct, and improve. I'm willing to preserve it as a Free To Use API, but not as an open-source project. Although, I may change my mind in the near future.

## Contact

If you have any questions or would want to contact me, please do so using any of the social platforms listed below.

> **Developed And Maintained By SecretsX**

> **Discord : Kanao#5758**

> **Twitter : @4R3T3**
