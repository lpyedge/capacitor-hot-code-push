# capacitor-hot-code-push

Installation
This requires capacitor 1.0+ (current stable 1.6.0)


首先要安装

在capacitor项目目录执行以下命令
1.下载安装plugin
npm i git+https://github.com/lpyedge/capacitor-hot-code-push.git
2.同步
npx cap sync
3.创建json和指纹文件（需要安装cordova-hot-code-push-cli并进行相关配置，参见https://github.com/nordnet/cordova-hot-code-push-cli）
cordova-hcp build

记得要修改对应platform下的config.xml文件
添加chcp相关节点配置

    <chcp>
        <auto-download enabled="false" />
        <auto-install enabled="false" />
        <native-interface version="1" />
        <config-file url="https://xxxx.com/ios/chcp.json" />
    </chcp>
