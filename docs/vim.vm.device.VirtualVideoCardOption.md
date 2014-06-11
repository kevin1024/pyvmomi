vim.vm.device.VirtualVideoCardOption
====================================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)


This data object type contains the options for the   <a href="vim.vm.device.VirtualVideoCard.md">VirtualVideoCard</a> data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| videoRamSizeInKB | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | true | None | Minimum, maximum and default size of the video frame buffer. |
| numDisplays | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | true | None | Minimum, maximum and default value for the number of displays. |
| useAutoDetect | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | true | None | Flag to indicate whether the display settings of the host should    be used to automatically determine the display settings of the    virtual machine's video card. |
| support3D | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | true | None | Flag to indicate whether the virtual video card supports 3D functions. |
| use3dRendererSupported | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | true | None | Flag to indicate whether the virtual video card can specify how to render 3D graphics. |


