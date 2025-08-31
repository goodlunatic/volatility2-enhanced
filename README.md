# Volatility2 Enhanced

结合社区和官方提供的，针对部分功能性完善的补丁，并且未合并进 Volatility2 main 分支的，进行修改后做的二次分发版本

## 修改内容

> 本仓库的 Volatility2 源码已针对相关问题进行如下修改

### 对 DWARF v5 提供支持

本修改参考自：

- [Linux Profile Error - KeyError: 'DW_AT_data_member_location' - volatilityfoundation/volatility Issue #828](https://github.com/volatilityfoundation/volatility/issues/828)
- [Added support for DWARF v5. - volatilityfoundation/volatility Pull Request #854](https://github.com/volatilityfoundation/volatility/pull/854)

本修改，对 `volatility/dwarf.py` 文件进行了修改，对 Volatility2 的 Linux DTB 扫描器部分进行修改

### 对 Linux 较新版本的内核提供支持

本修改参考自：

- [Linux Profile Error - KeyError: 'DW_AT_data_member_location' - volatilityfoundation/volatility Issue #828](https://github.com/volatilityfoundation/volatility/issues/828)
- [Update Linux DTB scanner to handle newer Linux kernel versions (>= 5.14-rc1) - volatilityfoundation/volatility Pull Request #852](https://github.com/volatilityfoundation/volatility/pull/852)

### 由于对较旧的 Linux 内核使用了最新版本的 **dwarfdump** 导致出现 `ValueError: invalid literal for int() with base 10`

本修改参考自：

- [Abyss-W4tcher/volatility2-profiles - Volatility patches](https://github.com/Abyss-W4tcher/volatility2-profiles?tab=readme-ov-file#volatility-patches)


### 修复 KeyError: '__int128 unsigned'

本修改参考自：

- https://github.com/volatilityfoundation/volatility/issues/478
