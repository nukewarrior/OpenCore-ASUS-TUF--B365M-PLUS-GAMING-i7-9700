# OpenCore-ASUS-TUF--B365M-PLUS-GAMING-i7-9700

- 硬件配置

  - 主板：ASUS-TUF-B365M-PLUS-GAMING
  - CPU：i7 9700
  - GPU：5700xt

- BIOS设置

- 使用方法

  - 制作OpenCore安装U盘，拷贝EFI文件夹至U盘BOOT分区，参考视频 [Intel Coffee Lake平台完美黑苹果系统安装教程](https://www.bilibili.com/video/BV1hA411t7dr)

  - 通过 [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS "GenSMBIOS") 生成自己的SMBIOS填入 `config.plist -> PlatformInfo` 中， 如果和我一样的配置，请选择iMac19,1

  - 删除 `EFI -> OC -> Kexts -> USBports.kext`

- 最后完善

  - 定制你自己的USB，参考视频：[黑苹果定制USB教程简易版，2步搞定USB定制](https://www.bilibili.com/video/BV1rt4y1y7Pb)
  - 如果iMessage·FaceTime不能正常启用，参考 [Fixing iService](https://dortania.github.io/OpenCore-Desktop-Guide/post-install/iservices.html) 修改自己的SMBIOS

- 注意⚠️

	- 我开启了BIOS中的`vt-D`功能，所以`config.plist`中的`Kernel->Quirks->DisableIoMapper`设置为`True`，如果你不需要`vt-D`可以将这个选项设置为`False`
