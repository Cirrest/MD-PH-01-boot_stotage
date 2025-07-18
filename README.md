# MOONDROP MD-PH-01 Phone System Update and Boot Stotage<br>水月雨 MD-PH-01 手机 系统更新和Boot存档<br><br>

声明：该项目仅本个人作存储官方公开的boot.img和update文件，方便用户恢复及存档升级使用，不做任何形式的修改、反编译、开源。著作权、商标等归[成都水月雨科技有限公司](https://moondroplab.com/)所有。
----

水月雨 MOONDROP MIAD01 手机 官方原厂boot及update升级文件<br>
<br>
相关更新日志可在水月雨MoonDrop 酷安/微博/微信公众号 查看
<br>

boot文件<br>

* 文件格式:boot_x_OSxxxxxx_ASW2301_CM_1201_Txxxx.img
  * boot_对应A/B槽位_对应增量升级包版本_关于手机中自定义版本号.img
  * ❗请注意，文件名的boot_A/B是按照本人从出厂版本逐个更新后的槽位，仅供参考。请用相关软件(如Devcheck)查看你的系统A/B槽位！<br>
  * 不要刷错！

 <br>
 update增量OTA更新包<br>
 
* Txxxx_to_Txxxx.zip
  * 目前版本_to_目标更新版本.zip 

### 请注意，Unlock Bootloader可能会导致发生不可预见的软/硬件问题，并且可能导致你失去售后权利保障等，本人不对此负责。
<br>
<br>

如何使用？
----

 ### 【Update增量OTA更新包】<br>

* update增量OTA更新包下载至手机内部存储中，在设置-系统-系统更新-右上角-本地更新-选择Txxxx_to_Txxxx.zip
    #####  请注意，OTA增量更新前请先核对你的目前手机系统自定义版本号与目标更新版本
boot文件<br>
如果你需要Root或需要修改boot，可以patch你的boot并刷入设备<br>

### 【Unlock Bootloader】
  *  使用你的电脑，提前装好adb与fastboot驱动。
  *  确认你所需要刷写boot对应的A/B分区以及对应分区版本，且需要Bootloader lock状态为Unlock<br>
    Unlock Bootloader<br>
    ```
   fastboot flashing unlock
    ```
### 【Lock Bootloader】(请确保所有分区均为官方镜像并无任何改动)<br>
   ```
   fastboot flashing lock
   ```
### 【刷入boot】
  *  使用fastboot命令行工具，手机在fast boot模式中键入以下命令<br>
    ```
    fastboot flash boot_a或b 你的文件位置
    ```
  *  刷写完成后键入以下命令重新启动你的手机并开始享受<br>
    ```fastboot reboot```
<br>
