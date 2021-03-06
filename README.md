VideoPlayerPlugin
===========

iOSでMovieを再生するためのプラグインです

[![ScreenShot](https://dl.dropboxusercontent.com/u/153254465/%E7%94%BB%E5%83%8F%E3%81%A8%E3%81%8B/Screen%20Shot%202013-08-09%20at%202.14.26.png)](http://youtu.be/SXHp_ztFksM)

##Functions
|Name|Description|
|:---|:---|
|PlayView|Viewで再生する|
|PlayTexture|Textureで再生する|
|Pause|一時停止|
|Resume|リジューム|
|Stop|停止|


###public void PlayView(Rect margin, string videoURL)</br>public void PlayView(int left, int top, int right, int bottom, string videoURL)
SubViewで再生を行います

videoURLはhttp/httpsかStreamingAssetsフォルダからの相対パス

```
if (GUILayout.Button("<size=42>ViewPlay</size>", GUILayout.Height(200)))
{
    video.Stop();
    video.PlayView(12, Screen.height / 2 + 12, 12, 12, "movie.mp4");
}
```


![](https://dl.dropboxusercontent.com/u/153254465/%E7%94%BB%E5%83%8F%E3%81%A8%E3%81%8B/2013-08-08%2023.34.31.png)

### public void PlayTexture(string videoURL, Material material = null)
マテリアルにVideoTextureを貼り付けます

materialがnullの場合は自分のMeshRendererにあるMaterialを使用します

videoURLはhttp/httpsかStreamingAssetsフォルダからの相対パス

![](https://dl.dropboxusercontent.com/u/153254465/%E7%94%BB%E5%83%8F%E3%81%A8%E3%81%8B/2013-08-08%2023.34.36.png)

```
if (GUILayout.Button("TexturePlay", GUILayout.Height(200)))
{
    video.PlayTexture("movie.mp4");
}
```

#Variables
|Name|Description|
|:---|:---|
|ready|再生可能かどうか|
|videoTexture|Texture再生時のTexture|
|videoSize|ビデオサイズ|
|duration|動画の長さ|
|isPlaying|再生中かどうか|





