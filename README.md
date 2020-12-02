# cesium-videoshed
基于cesium视频投射

----------------------------------------------------------------------------------------------------------------------------------------
### 基于cesium的3dtilset模型视频投放
### cesium-videoshed

### 说明
##### /cesium-videoshed/src/doc

### 使用

#####  在项目中引入Cesium.js

#####  然后引入 cesium-videoshed.js 即可

<a href="http://zhangticcc.gitee.io/webgis/"><img alt="" height="100%" src="https://img-blog.csdnimg.cn/20201202172350462.gif" width="90%" ></a>&nbsp;

``` 
    // 初始化
    let viewer = new Cesium.Viewer("viewerContainer")

    // 参数
    let viewModel = { verticalAngle: 90, horizontalAngle: 120, distance: 10 };
    let videoShed3DArr = [];

    // 创建
    let create = () => {
        let videoShed3D = new Cesium.VideoShed3D(viewer, {
          type: 'Video',
          url: "src/cs.mp4",
          alpha: 1,
          debugFrustum: true,
          horizontalAngle: Number(viewModel.horizontalAngle),
          verticalAngle: Number(viewModel.verticalAngle),
          distance: Number(viewModel.distance),
        });
        videoShed3DArr.push(videoShed3D)
    }
    // 销毁
    let destroy = () => {
        videoShed3DArr.forEach(video => video.destroy())
    }
```
