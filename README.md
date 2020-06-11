# OpenCore-ASUS-TUF--B365M-PLUS-GAMING-i7-9700

- 硬件配置

  - 主板：ASUS-TUF-B365M-PLUS-GAMING
  - CPU：i7 9700
  - GPU：5700xt

- BIOS设置

  - 关闭

  ```(bash)
  Fast Boot
  CSM
  Intel SGX
  CFG Lock
  ```

  - 打开

  ```(bash)
  VT-x
  VT-D
  Above 4G decoding
  OS Type:other
  ```

- 使用方法

  - 制作OpenCore安装U盘，拷贝EFI文件夹至U盘BOOT分区，参考视频： [Intel Coffee Lake平台完美黑苹果系统安装教程](https://www.bilibili.com/video/BV1hA411t7dr)

  - 通过 [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS "GenSMBIOS") 生成自己的SMBIOS填入 `config.plist -> PlatformInfo` 中， 如果和我一样的配置，请选择iMac19,1

- 最后完善

  - 定制你自己的USB，参考视频：[黑苹果定制USB教程简易版，2步搞定USB定制](https://www.bilibili.com/video/BV1rt4y1y7Pb)
  - 如果iMessage·FaceTime不能正常启用，参考 [Fixing iService](https://dortania.github.io/OpenCore-Desktop-Guide/post-install/iservices.html) 修改自己的SMBIOS
  - 去除debug信息显示，教程：[Fixing Resolution and Verbose](https://dortania.github.io/OpenCore-Desktop-Guide/post-install/verbose.html)
  - 为oc引导菜单添加GUI支持(感觉没用，电脑启动后用的是系统，并不是引导菜单🐶)，教程：[OpenCore beauty treatment](https://dortania.github.io/OpenCore-Desktop-Guide/extras/gui.html)

- 注意⚠️

  - 我开启了BIOS中的`vt-D`功能，所以`config.plist`中的`Kernel->Quirks->DisableIoMapper`设置为`True`，如果你不需要`vt-D`可以将这个选项设置为`False`
  - 我定制了USB后感觉台式机没啥大用，而且这个定制是因人而异不能通用的，所以这个repo里的并没有定制USB
