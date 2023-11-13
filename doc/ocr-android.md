# ocr-android文本识别

## 1.0.0

## 使用CameraX + MLKit机器学习套件实现。

 - [x] 支持护照机读码识别（MRZ码）
 - [x] CameraX自带生命周期管理
 - [x]  Android5.0及以上



# 使用前申请相关权限
```
Manifest.permission.CAMERA
```
# 识别
```

    /**
     * 开始扫描
     */
    private fun startScann() {
        ScanningManager.instance.openScanningActivity(this@MainActivity, Config(true, ScanTypeEnum.PASSPORT_MRZ, 
                object :ScanResultListener{
                    override fun onSuccessListener(value: String?) {
                        // 识别结果
                    }

                    override fun onFailureListener(error: String) {
                        // 识别失败
                    }
                }))
    }


 # Config 参数说明

Config(
    /**
     * 是否循环识别，等待识别结果
     */
    val isLoopWaitResult: Boolean = true,
    /**
     * 识别类型
     */
    val scanType: ScanTypeEnum = ScanTypeEnum.PASSPORT_MRZ,
    /**
     * 结果回调
     */
    val scanResultListener: ScanResultListener? = null
)
```
