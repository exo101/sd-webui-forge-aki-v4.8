# Stable Diffusion WebUI Forge 整合包使用说明

旧整合包已不适用日益更新的AI应用与50系显卡，为此我更新了新整合包环境，补充落后的webui Forge生态
对于ComfyUI复杂的节点连线式操作界面，对新手确实不太好学习。WebUI Forge更加易操作，直观好理解，适合入门

## 整合包内部多模态插件支持 
|`nunchaku`| `qwen-image-edit2509`|`qwen-image`|`qwen-image-ControlNet`|`qwen lora` |
|`qwen3` |`qwen3VL`|`qwen2.5VL`| `Ollama`|`llama3.2-vision`|
|`LatentSync` |`Segment Anything`|`Cleaner`|`Index-TTS2` |
|`FLUX.1-Kontext` | `FLUX` |`不支持FLUX ControlNet` | `XL` | `XL ControlNet` |`sd15 ControlNet`|`sd15`|

## 系统要求

- 显卡：最低推荐 NVIDIA RTX 3060 12gb
- 显存：推荐 12GB，内存：推荐 64GB
- 推荐的显卡NVIDIA系列：3080,3090,4060ti,4070，4070TI,4080,4090
- 5060TI,5070,5070TI,5080,5090

- Qwen-Image: 12GB /内存64g
- Qwen3vL: 10GB
- Z-Image-Turbo:12g//内存32g
- Segment Anything: 10GB
- Cleaner: 8GB
- LatentSync: 12GB
- Index-TTS: 12GB
- FLUX.1-Kontext:8GB
- FLUX-krea:8GB
- FLUX:8GB
- XL: 8GB
- roop：8GB



## 下载地址可查看个人主页视频简介下方：

[https://www.bilibili.com/video/BV1BCHXzJE1C/?spm_id_from=333.788.videopod.sections&vd_source=343e49b703fb5b4137cd6c1987846f37](https://www.bilibili.com/video/BV1FWtBzbEiR?spm_id_from=333.788.player.switch&vd_source=343e49b703fb5b4137cd6c1987846f37&trackid=web_related_0.router-related-2206419-r6wc2.1760535637914.805) 


- 1.安装使用7z2501-x64.exe压缩软件进行解压整合包
- 2.首次使用整合包需要安装启动器运行依赖-dotnet-6.0.11.exe
- 3.整合包自带虚拟环境python，git，cuda，xFormers，PyTorch，transformers，无需下载依赖任何文件
- 4.每次更新整合包版本，只需迁移根目录下旧整合包moders即可，其余内容全部删除
- 5.所有插件与整合包都在百度网盘当中，qq群内交流ai技术1054090769  


| 整合包目录 | 模型目录 | 子目录 |说明 |
|---------------------|--------|-----------|-----------|
| `sd-webui-forge-aki`|`models`|`adetailer`| 修脸插件模型 |
| `sd-webui-forge-aki`|`models`|`cleaner`| 图像清理模型目录 |
| `sd-webui-forge-aki`|`models`|`RealESRGAN`| 高清放大算法目录 |
| `sd-webui-forge-aki`|`models`|`ESRGAN`| 高清放大算法目录 |
| `sd-webui-forge-aki`|`models`|`lora`| LoRA微调模型目录 |
| `sd-webui-forge-aki`|`models`|`LatentSync`| 数字人视频生成模型目录 |
| `sd-webui-forge-aki`|`models`|`qwen-image`| qwen模型与组件总目录 |
| `sd-webui-forge-aki`|`models`|`index-tts2`| Index-TTS语音合成模型目录 |
| `sd-webui-forge-aki`|`models`|`FLUX.1-Kontext-dev`| nunchuku量化fluX系列模型目录 |
| `sd-webui-forge-aki`|`models`|`ControlNet`| ControlNet控制模型目录 |
| `sd-webui-forge-aki`|`models`|`ControlNetPreprocessor`| ControlNet预处理器目录 |
| `sd-webui-forge-aki`|`models`|`insightface`| 换脸插件模型 |
| `sd-webui-forge-aki`|`models`|`faceswaplab`| 换脸插件模型 |
| `sd-webui-forge-aki`|`models`|`GFPGAN`| 换脸插件放大模型 |
| `sd-webui-forge-aki`|`models`|`Codeformer`| 换脸插件放大模型 |
| `sd-webui-forge-aki`|`models`|`roop`| 换脸插件模型目录 |
| `sd-webui-forge-aki`|`models`|`sam`| 图像分割模型目录 |
| `sd-webui-forge-aki`|`models`|`Stable-diffusion`| 传统flux.XL.1.5模型目录 |
| `sd-webui-forge-aki`|`models`|`Tongyi-MAl`| Z-Image模型目录 |
| `sd-webui-forge-aki`|`models`|`vae`| 图像编解码模型 |


| 整合包目录 |插件路径 |
| `sd-webui-forge-aki`|`extensions` |插件目录|
| `sd-webui-forge-aki`|`outputs` |图像输出目录|
| `sd-webui-forge-aki`|`extensions\sd-ppp-1.5.4` |
| `sd-webui-forge-aki`|`extensions\Auto-Photoshop-StableDiffusion-Plugin` |ps ai插件| 
| `sd-webui-forge-aki`|`extensions\sd-webui-reactor` |换脸插件 |
| `sd-webui-forge-aki`|`extensions\sd-webui-roop` |换脸插件 |
| `sd-webui-forge-aki`|`extensions\sd-webui-MultiModal` | 多模态插件 |


## 更新内容
2025/12/12
- flux系列模型全面支持nuachaku量化加速，如Kontext，flux-krea，flux
- 4.9整合包安装了sageattention与Triton优化加速
- sageattention和Triton优化，需要Windows编译软件进行破译，需要安装Windows SDK，Visual Studio

2025/12/8
- 4.8整合包删除过时无用的插件，精简ui界面
- 部署Z-Image-Turbo模型
  
- 4.7整合包修复了旧插件与webui froge的兼容
- 增加换脸插件 sd-webui-reactor
- 增加换脸插件 sd-webui-roop
- 增加psai插件 sd-ppp
- 增加无边浏览图像插件 sd-webui-infinite-image-browsing
  

2025/11/14
- 整合包增加了ui交互指南，降低了使用难度，参数科普，各类模型加载方式，快捷描述方式
- 增加FLUX加速lora放到了网盘插件模型的lora目录中，Hyper-FLUX.1-dev-8steps-lora，大大降低生成时间
- <img width="1852" height="538" alt="QQ20251114-221008" src="https://github.com/user-attachments/assets/94e8a632-1052-4c62-b652-2b1ee0748ee3" />
  <img width="736" height="527" alt="QQ20251114-221148" src="https://github.com/user-attachments/assets/acf98dfe-52d7-4155-a6ae-1e24cad48b60" />

 2025/10/31
- 添加nunchaku-qwen-image-edit-2509 lora功能加载
- 添加一致性场景lora模型，pytorch_lora_weights.safetensors
- qwen-image文生图模型lora，也可以应用到编辑模型当中
  
2025/10/29
- 更新至sd-webui-forge-aki-v4.5版本
- 增加qwen-image lora功能实现，qwen-image ControlNet分类多变体预处理器，排除不支持的类别防止误操作
- 更新了nunchaku加速轮子版本，已修改diffusion底层代码，后续有时间会全面应用插件中，nunchaku版本模型大幅降低flux模型生成时间
  
2025/10/24 
- sd-webui-forge-aki-v4.4版本
- 更新完善qwen-image ControlNet实现多个变体预处理器
- 支持qwen3VL需要transformers==4.57.0版本，但会牺牲Index-TTS2语音合成功能使用
- Index-TTS2需要transformers==4.52.1版本，但会牺牲qwen3VL，两者存在冲突
- 修改根目录requirements_versions配置文件transformers版本即可

2025/10/20
- 更新至webui-forge-aki-v4.3版本
- 修复 1.5 ControlNet与XL ControlNet 预处理器bug，promax版本可同时实现线稿，深度，姿势，软边缘，不必下载任何XL ControlNet模型
- 添加了综合性XL ControlNet 模型以及预处理器至网盘controlnet-union-sdxl-1.0_promax.safetensors
  
2025/10/18 
- 更新至sd-webui-forge-aki-v4.2
- 更新了diffusers==0.36.0.dev0
- 增加nunchaku量化库安装了加速轮子大大提高了qwen模型生成速度
- 多模态插件12 更新了qwen-image ControlNet，同时实现了深度，姿势，线稿，软边缘
- ControlNet模块不支持FLUX ControlNet模型，新整合包修复了ADetailer修脸插件，wd1.4标签器等bug

### GPU 显存管理
- GPU Weights(MB)滑动条数值是显存的容量
- 往左滑动是模型权重加载，往右是模型计算空间
- 正常情况下，右滑动过半，留出20%-40%的计算空间
- 如果模型权重预留的空间不足，模型会加载失败
- 如果模型计算空间不足，会生成时间变慢，程序崩溃爆显存

<img width="1720" height="165" alt="11" src="https://github.com/user-attachments/assets/45008dd6-cb33-41f4-b9a2-a312d388cc61" />

## 各类模型加载方式
  示例视频：https://www.bilibili.com/video/BV1HseizrEQs?spm_id_from=333.788.videopod.sections&vd_source=343e49b703fb5b4137cd6c1987846f37
  
### FLUX模型加载方式
  需要以下模型文件：
- 主模型: `flux1-dev-fp8.safetensors`          目录| `sd-webui-forge-aki-v4.0\models\Stable-diffusion` |
- 文本编码模型: `t5xxl_fp8_e4m3fn.safetensors` 目录| `sd-webui-forge-aki-v4.0\models\VAE` |
- CLIP模型: `clip_l.safetensors`               目录| `sd-webui-forge-aki-v4.0\models\VAE` |
- VAE模型: `flux-ae.safetensors`               目录| `sd-webui-forge-aki-v4.0\models\VAE` |
- flux参数设置：采样方法Euler，调度器Simple， CFG引导数3.5，迭代步数20-35
<img width="1600" height="95" alt="24" src="https://github.com/user-attachments/assets/c94d496a-ad36-4218-9803-8fdaa986677e" />
<img width="910" height="348" alt="123" src="https://github.com/user-attachments/assets/2f0b6081-ba91-454c-a4ef-8136f43a0373" />

### XL模型加载方式

- 主模型（约6GB)Dream Anime XL _ 筑梦动漫XL_v2.0 - 漫笔爱恋 目录 | `sd-webui-forge-aki-v4.0\models\Stable-diffusion` |
- VAE模型: `sdxl_vae.safetensors`                          目录 | `sd-webui-forge-aki-v4.0\models\VAE` |
- XL参数设置：采样方法DPM++ 2M SDE，调度器Karras， CFG引导数7，迭代步数20-35
  <img width="1092" height="810" alt="25" src="https://github.com/user-attachments/assets/c52b9db3-fcc7-4c58-8434-adc0a306a6b6" />

### 1.5模型
- 主模型（约2.3GB) hellopure_V30a 目录 | `sd-webui-forge-aki-v4.0\models\Stable-diffusion` |
- 参数与XL无差别
- VAE模型: `vae-ft-mse-840000-ema-pruned.safetensors`目录| `sd-webui-forge-aki-v4.0\models\VAE` |
  
### 高清放大模型参数设置

低配置用户需要调低基础尺寸，开启放大2倍，如果基础尺寸很大，放大倍数就要调低，模型参数越大放大的尺寸需要的显存压力也会越大
<img width="880" height="187" alt="22" src="https://github.com/user-attachments/assets/d9936900-fea9-43e8-928d-bf1ef6721582" />

高清放大算法介绍



### ControlNet使用说明

 如 control_v11p_sd15s2_lineart_anime.pth标识带有sd15就是1.5模型使用的，而1.5大模型只有2gb左右
 如 controlnet-union-sdxl-1.0_promax.safetensors标识sdxl就是XL模型使用的，而XL模型大约6gb左右

在我视频简介下方提供的下载链接中提供的controlnet模型和预处理器是不全的，缺少的自行下载，我下载的是常用的，不常用的就没有下载
不建议折腾IP-Adapter预处理器，这个预处理器高达十几个版本的模型，相互的对应关系冗长复杂，名称更是繁多，需要颇费一番功夫才能知道了解清楚
如今已有换脸插件代替IP-Adapter预处理代替了这个换脸功能，风格迁移已由qwen的编辑模型使用lora可以更好的实现

<img width="859" height="766" alt="123123" src="https://github.com/user-attachments/assets/f516969f-5cb4-4aab-a812-437e751d5520" />

推荐使用controlnet-union-sdxl-1.0_promax.safetensors，这是一个综合型ControlNet模型，包括了深度，线稿，open pose

使用ControlNet模型时记得查看模型之间的对应关系，1.5大模型对应1.5的ControlNet模型，XL大模型对应XL的ControlNet模型 

ControlNet使用由预处理器和ControlNet模型共同协作才能完成，缺少哪一个，或者预处理器与模型关系不对应都会出现错误

大多数人出现的错误就是缺少预处理器，或者网络无法链接下载

<img width="1278" height="786" alt="12431243243" src="https://github.com/user-attachments/assets/aa986e32-fe26-45ad-a5f7-cbc7f48142d5" />
查看后台日志，会提示你出现了那些错误，比如我使用了depth_anything这个预处理器，出现了错误

Downloading: "https://huggingface.co/spaces/LiheYoung/Depth-Anything/resolve/main/checkpoints/depth_anything_vitl14.pth" to D:\sd-webui-forge-aki-v4.0\models\ControlNetPreprocessor\depth_anything\depth_anything_vitl14.pth
Traceback (most recent call last):
  File "D:\sd-webui-forge-aki-v4.0\python\Lib\site-packages\urllib3\connection.py", line 198, in _new_conn
    sock = connection.create_connection(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "D:\sd-webui-forge-aki-v4.0\python\Lib\site-packages\urllib3\util\connection.py", line 85, in create_connection
    raise err
  File "D:\sd-webui-forge-aki-v4.0\python\Lib\site-packages\urllib3\util\connection.py", line 73, in create_connection
    sock.connect(sa)
TimeoutError: [WinError 10060] 由于连接方在一段时间后没有正确答复或连接的主机没有反应，连接尝试失败。

那么就应该搜索这个模型depth_anything_vitl14.pth，自行下载到预处理目录

<img width="1327" height="960" alt="46456547" src="https://github.com/user-attachments/assets/c75a1022-7aca-4b03-9054-a93962876c7a" />
<img width="1274" height="522" alt="34478" src="https://github.com/user-attachments/assets/cebf370f-9561-4d6a-a953-cb6e5ac3c93e" />

现在就没有了错误

<img width="1797" height="844" alt="45644" src="https://github.com/user-attachments/assets/56a6c2ed-c187-4ce6-b713-ce7be41ee264" />



### wd1.4标签器插件
- 选择模型wd14-vit-v2-git
- <img width="879" height="428" alt="66" src="https://github.com/user-attachments/assets/ec5cac8f-6ec7-434a-857a-1066908320ef" />
- <img width="1805" height="759" alt="77" src="https://github.com/user-attachments/assets/2b2caba2-a8e7-4327-a9c5-cc349a13a530" />
- 整合自带的标签器识别的提示词远不如Qwen-VL、LLaMA-Vision等视觉模型来的提示词质量与丰富，准确率很低，只方便与快速识别与制作二次元动漫人物
- 高质量提示词请使用多模态插件 https://github.com/exo101/sd-webui-MultiModal

