 # Win7适配不完全指南
 
## 1. 前置准备

### 1.1 开发者

#### 1.1.1 rustc版本降低至 < 1.77.2
 
> [相关讨论](https://github.com/tauri-apps/tauri/issues/10008)

##### 不降版本会出现的报错
![启动报错](https://img.alicdn.com/imgextra/i4/O1CN015Rt9Nw1Gt1tnaHMsQ_!!6000000000679-0-tps-998-390.jpg "启动报错")

### 1.2 Win7用户

#### 1.2.1 安装Windows Update

> [x64下载地址](https://www.microsoft.com/en-us/download/details.aspx?id=48636)
> 
> [x86下载地址](https://www.microsoft.com/en-us/download/details.aspx?id=48638)

[相关讨论](https://github.com/tauri-apps/tauri/issues/5163)

##### 未安装时的报错
![启动报错](https://img.alicdn.com/imgextra/i3/O1CN01BfEseq27j6xOGYoWg_!!6000000007832-0-tps-842-364.jpg "启动报错")

### 1.2.2 安装windows sp1更新
> [下载地址](https://www.catalog.update.microsoft.com/Search.aspx?q=KB976932)

### 1.2.3 安装webview2
> [下载地址](https://go.microsoft.com/fwlink/p/?LinkId=2124703)

#### 可能存在的问题
![下载失败](https://img.alicdn.com/imgextra/i4/O1CN018o3xbj1dcIapCQ86t_!!6000000003756-2-tps-722-314.png "下载失败")
##### 解决方案
https://answers.microsoft.com/zh-hans/microsoftedge/forum/all/%E5%AE%89%E8%A3%85edge%E6%97%B6%E5%87%BA%E7%8E%B0/06976b47-4e4b-4efe-9a98-634ff06df873

## 2. tauri配置
### 2.1 webview2安装模式
```
{
  "tauri": {
    "bundle": {
      "windows": {
        "webviewInstallMode": {
          "type": "embedBootstrapper"
        }
      }
    }
  }
}
```

## 3. 相关文档
> https://github.com/tauri-apps/tauri/issues/7338
> https://github.com/tauri-apps/tauri/issues/2882






