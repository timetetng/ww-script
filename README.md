# 鸣潮抽卡记录获取脚本
# WutheringaWaves-script for getting gacha-logs

## 如何使用？

* **win + s** 打开 Windows 搜索栏
* 搜索 `powershell`
* 右键-以管理员身份打开
* 粘贴命令并回车执行即可：

  ```powershell
  irm ww.lsgbin.com/main | iex
  ```
  访问失败可能是网络问题，您也可以直接下载本仓库的 `ww-gacha-log` 文件，修改后缀为 `.ps1` 后，在 `powershell` 中运行


  ```powershell
  .\ww-gacha-log.ps1
  ```
  
* 预期输出：

  ```powershell
   [成功] 找到 'Client' 目录: E:\Wuthering Waves\Wuthering Waves Game\Wuthering Waves Game\Client
        ... 正在读取日志文件提取链接...
  ================= 找到抽卡链接 =================
  https://aki-gm-resources.aki-game.com/aki/gacha/index.html#/record?svr_id=76xx&player_id=1xxxxxxx2&lang=zh-Hans&gacha_id=xx&gacha_type=1&svr_area=cn&record_id=3dc489354asd46a95fxed14f&resources_id=0bd52af4347779d0fc32400&platform=PC
  ===============================================
  抽卡链接已复制到剪贴板
  --- 脚本执行完毕 ---
  ```
* 可能的情况：
  - **未找到游戏路径**:
    
    通常是因为您游戏路径不放在盘符根目录导致检索失败。
    此时会弹出手动模式，需要您输入 `Client` 目录所在的**根目录路径**，此目录下通常还有 `Wuthering Waves.exe`。如果您不清楚安装路径，可以打开启动器 **设置-游戏** 查看。
  - **未找到日志文件或抽卡记录**:
  
    此情况多半是您未预先登录游戏并打开唤取记录，请打开后多翻页几次再重新执行脚本。
