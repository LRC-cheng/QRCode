# QRCode

by--Asting
2019.07.12

这是基于ZXing做的扫一扫功能，在之前的shortcut项目基础上增加的功能
主要涉及以下步骤：
1.导入core-3.3.0 jar包
2.把ZXing的ZxingLibary文件夹下的资源文件、代码文件复制到自己的项目，修改java文件里的R包等依赖包的路径
3.根据需要修改activity_capture的界面
4.修改注册文件AndroidManifest.xml，添加CaptureActivity
5.调用，需要申请照相机权限，参考Permission库的使用

调用方式：
                Intent intent = new Intent(MainActivity.this, CaptureActivity.class);
                ZxingConfig config = new ZxingConfig();
                config.setPlayBeep(false);
                config.setShake(false);
                intent.putExtra(Constant.INTENT_ZXING_CONFIG, config);
                startActivityForResult(intent, REQUEST_CODE_SCAN);
