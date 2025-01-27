简体中文 | [English](./README_EN.md)

> [!IMPORTANT]
> ## 
随便修改玩玩
### 👀 Demo
### 🎉 功能

- [x] 载入动画
- [x] 站点简介
- [x] Hitokoto 一言
- [x] 日期及时间
- [x] 实时天气
- [x] 时光进度条
- [x] 音乐播放器
- [x] 移动端适配


#### 字体进一步压缩

- 编译安装 `Google woff2`

```bash
sudo apt-get install -y git g++ make
git clone --recursive https://github.com/google/woff2.git
cd woff2
make clean all
```

- 再压缩字体

```
./woff2_compress ./字体名称.ttf
```

- 最终可对原字体进行缓加载，**先行加载压缩后的字体**

> 详细信息可前往 [虹墨空间站](https://www.imaegoo.com/2020/chinese-font-compress/) 查看原文

</details>

### 网站图标及网站背景

#### 网站背景

可以在 `public/images` 中修改网站背景

如果想要添加更多的本地图片作为网站背景，可以将图片重命名 `background+数字` 的形式，并在 `src/components/Background/index.vue` 中进行修改：

```js
if (type == 0) {
  // 修改此处 Math.random() 后面的第一个数字为图片的数量
  bgUrl.value = `/images/background${Math.floor(Math.random() * 10 + 1)}.webp`;
}
```

#### 网站图标

可以在 `public/images/icon` 中修改网站图标。

### 技术栈

- [Vue](https://cn.vuejs.org/)
- [Vite](https://vitejs.cn/vite3-cn/)
- [Pinia](https://pinia.vuejs.org/zh/)
- [IconPark](https://iconpark.oceanengine.com/official)
- [xicons](https://xicons.org/)
- [Aplayer](https://aplayer.js.org/)

### API

- [韩小韩 WebAPI 接口](https://api.vvhan.com/)
- [搏天 API](https://api.btstu.cn/doc/sjbz.php)
- [教书先生 API](https://api.oioweb.cn/doc/weather/GetWeather)
- [高德开放平台](https://lbs.amap.com/)
- [Hitokoto 一言](https://hitokoto.cn/)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=imsyy/home&type=Date)](https://star-history.com/#imsyy/home&Date)

<a title="SSL" target="_blank" href="https://myssl.com/seal/detail?domain=blog.imsyy.top"><img src="https://img.shields.io/badge/MySSL-安全认证-brightgreen"></a>&nbsp;<a title="CDN" target="_blank" href="https://cdnjs.com/"><img src="https://img.shields.io/badge/CDN-Cloudflare-blue"></a>&nbsp;<a title="Copyright" target="_blank" href="https://imsyy.top/"><img src="https://img.shields.io/badge/Copyright%20%C2%A9%202020--2023-%E7%84%A1%E5%90%8D-red"></a>
