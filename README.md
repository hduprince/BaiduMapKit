# BaiduMapKit

百度地图 iOS SDK(官方)

--------------------------------------------------------------------------------------

iOS 地图 SDK v4.2.1是适用于iOS系统移动设备的矢量地图开发包

--------------------------------------------------------------------------------------

地图SDK功能介绍（全功能开发包）：

地图：提供地图展示和地图操作功能；

POI检索：支持周边检索、区域检索和城市内兴趣点检索；

地理编码：提供经纬度和地址信息相互转化的功能接口；

线路规划：支持公交、驾车、步行三种方式的线路规划；

覆盖物图层：支持在地图上添加覆盖物（标注、几何图形、热力图、地形图图层等），展示更丰富的LBS信息；

定位：获取当前位置信息，并在地图上展示（支持普通、跟随、罗盘三种模式）；

离线地图：使用离线地图可节省用户流量，提供更好的地图展示效果；

调启百度地图：利用SDK接口，直接在本地打开百度地图客户端或WebApp，实现地图功能；

周边雷达：利用周边雷达功能，开发者可在App内低成本、快速实现查找周边使用相同App的用户位置的功能；

LBS云检索：支持查询存储在LBS云内的自有数据；

特色功能：提供短串分享、Place详情检索、热力图等特色功能，帮助开发者搭建功能更加强大的应用；


--------------------------------------------------------------------------------------
 
 
 【 温 馨 提 示 】
 【 注 意 】
 1、自v3.2.0起，百度地图iOS SDK全面支持HTTPS，需要广大开发者导入第三方openssl静态库：libssl.a和libcrypto.a（存放于thirdlib目录下）
 添加方法：在 TARGETS->Build Phases-> Link Binary With Libaries中点击“+”按钮，在弹出的窗口中点击“Add Other”按钮，选择libssl.a和libcrypto.a添加到工程中 。
 
 2、支持CocoaPods导入
 pod setup //更新CocoPods的本地库
 pod search BaiduMapKit  //查看最新地图SDK
 

V4.2.1版本：

【新 增】
1.BMKAnnotationView新增hidePaopaoWhenSingleTapOnMap、hidePaopaoWhenDrag、displayPriority等新字段，提供更灵活的控制annotationView和paopaoView显示层级的解决方案。
2.BMKMapview新增 mapView:regionWillChangeAnimated:reason:和 mapView:regionDidChangeAnimated:reason: 两个回调，其中reason说明本次地图区域发生变化是由何种原因触发的。
3.BMKMapview的方法selectAnnotation:animated:开始支持动画效果。
4.支持长按paopaoView拖动annotationView。
5.BMKLocationViewDisplayParam新增属性locationViewImage，支持由开发者提供定位图标的图片。

【优 化】
1.提升底图加载渲染速度。
2.提升拖动地图时annotationView随地图移动的平滑度。

【修 复】
1.修复多页面多瓦片图切换时，瓦片图加载不出来的问题。
2.修复断网后应用退到杀进程界面，从杀进程界面进入应用，进行重复多次会导致手机重启的问题。
3.修复步行导航退出导航后，外部地图无法滑动的问题。
4.修复地图比例尺可能会超出屏幕边界的问题。
5.修复首次进入地图滑动地图没有mapView:regionWillChangeAnimated回调的问题。
6.修复屏幕上添加固定标注后，showAnnotations方法显示不准确的问题。
7.修复地图点击时，region没有发生变化，但是会触发regionchange回调的问题。
8.修复用户按住某个annotation缩放或拖动过程中，会触发didSelectAnnotationView而不触发regionDidChangeAnimated的问题。
