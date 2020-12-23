## 下载
1. 下载MATLAB R2018a for Linux full crack文件,云盘共享地址

链接: https://pan.baidu.com/s/1W6jWkaXEMpMUEmIl8qmRwg 密码: igx6

## 安装
2. 进入下载后的文件夹(假如下载后的文件放在了/home/deeppf中,其中deeppf是用户名)解压破解文件Matlab2018aLinux64Crack.tar.gz文件,创建一个文件夹Crack来放置解压后的文件


```
cd ~
sudo mkdir Crack
```
解压文件:


```
cd ~
tar -xvf Matlab2018aLinux64Crack.tar.gz -C Crack
```

3. 在/mnt中创建一个文件夹用来挂载R2018a_glnxa64_dvd1.iso和R2018a_glnxa64_dvd2.iso

```
cd /mnt
sudo mkdir iso
```
4. 先挂载R2018a_glnxa64_dvd1.iso
```
cd ~ # 到R2018a_glnxa64_dvd1.iso目录下
sudo mount -t auto -o loop R2018a_glnxa64_dvd1.iso /mnt/iso
```

如果这个时候提示/mnt/iso: WARNING:device write-protected,mounted read-only,那就修改下/mnt的权限

```
cd /
sudo chmod 755 mnt
```
5. 安装开始,从挂载的文件夹iso中


```
cd /mnt/iso
sudo./install
```
注意：这个时候可能会出现"无法从DVD目录内部运行安装程序，请到主目录下/mnt/iso/install",操作：

```
cd ..
sudo ./iso/install
```
然后，出现交互界面，具体安装过程:

1. 选择 Use a File Installation Key  
2. 选择Yes,同意条约  
3. 选择默认安装目录,默认放在/usr/local中  
4. 选择I have the File Installation Key for my license.  
输入:09806-07443-53955-64350-21751-41297  
5. 安装到某个进度（60%）会提示插入iso2,这个时候挂载R2018a_glnxa64_dvd2.iso

打开一个新的命令窗：

```
cd ~  # 到R2018a_glnxa64_dvd2.iso目录下
sudo mount -t auto -o loop R2018a_glnxa64_dvd2.iso /mnt/iso
```
6. 最后安装完成选择finish

## 破解
1. 复制破解文件Crack中license_standalone.lic到安装目录中

```
cd ~/Crack  
sudo cp license_standalone.lic /usr/local/MATLAB/R2018a/licenses
```

2. 复制Crack中的R2018a到安装目录

```
cd ~/Crack
cp -r R2018a /usr/local/MATLAB
```
## 创建快捷方式
采用软链接的方式在/usr/local/bin中创建启动命令matlab

```
cd /usr/local/bin
ln -s /usr/local/MATLAB/R2018a/bin/matlab matlab
```
## 删除多余文件

取消挂载,删除文件

```
umount /mnt/iso
cd /mnt
rmdir iso
```
此处可能会出现“删除 'iso' 失败: 设备或资源忙”

## 修改成windows方式快捷键

选择HOME > ENVIRONMENT > Preferences > Keyboard > Shortcuts；

然后把“Emacs Default Set”改成“Windows Default Set”.
## 使用
在任意路径输出matlab，即可打开,例如

```
deeppf@deeppf-Ubuntu:~$ matlab
```
