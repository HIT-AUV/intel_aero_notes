# 恢复被 Etcher 写过镜像的 U 盘

来源：[GitHub - Etcher - Recovering broken drives](https://github.com/resin-io/etcher/blob/master/docs/USER-DOCUMENTATION.md#recovering-broken-drives)

官方文档要求更新 OS 的时候使用 Ether（针对 Windows 用户）。Ether 刷过的 U 盘无法看到、无法格式化。只贴 Windows 的方法：

- Open cmd.exe from either the list of all installed applications, or from the "Run..." dialog usually accessible by pressing Ctrl+X.

- Type diskpart.exe and press "Enter". You'll be asked to provide administrator permissions, and a new prompt window will appear. The following commands should be run in the new window.

- Run list disk to list the available drives. Take note of the number id that identifies the drive you want to clean.

- Run select disk N, where N corresponds to the id from the previous step.

- Run clean. This command will completely clean your drive by erasing any existent filesystem.

- 用 Windows 磁盘管理对 U 盘新建分区并格式化。
