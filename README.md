建议开启格式-自动换行，效果更佳
注意
1.腾讯会议主程序目录默认为C:\Program Files (x86)\Tencent\WeMeet\wemeetapp.exe。如需修改路径，代码位置为：
    //这里改成自己的安装路径
    Process.Start(@"C:\Program Files (x86)\Tencent\WeMeet\wemeetapp.exe");
2.系统分辨率必须为1920X1080且缩放比例为100%，如需修改路径请利用Snipaste重新获取坐标点。LeftMouseClick(820, 319)，括号内内容即为坐标点。
3.预定会议日期格式为日/小时/分钟，如会议的预定日期为4月18日8时15分，格式为18/8/15，无需输入月份。
4.程序遵循开源协议，源码来自https://github.com/Yoroion/FuckTencentMeeting。不得用于商业用途。
5.该项目在@Yoroion的基础上修改，增加了进入带密码会议的功能，如需不带密码版本请直接使用@Yoroion的原版。

以下内容来自Yoroion的Github

# 📡 腾讯会议自动入会
使用 C#10 编写，自动进入会议，解放你的双手(

## 环境要求
- .NET 6.0+
- Windows 10+ 操作系统
- Visual Studio 2022 / VS Code + C# Extension

## 背景

- 因为疫情，学校停课，老师要求使用腾讯会议，我受到启发，写了这个小程序，顺便练练 C# 语言
- 逻辑就是设置时间，获取按钮所在的坐标，模拟鼠标点击和键盘输入
- 注意本程序默认基于 1080P 分辨率，其它分辨率可以使用 `Snipaste` 软件获取坐标
- 由于使用了 .NET Framework 的 NuGet 库，不能跨平台

## 文件说明
| 文件名            | 描述                |
| -----------      | -----------        |
| Program.cs       | 简单的主逻辑程序           |
| Win32Method.cs   | 封装了一些 Win32 API |

## 使用教程
1.  Clone 本项目
2.  在 `Program.cs` 中，修改腾讯会议的安装路径
![使用](./usage.png)
3. 使用 `Snipaste` 或其他软件获取需要按点击的坐标
4.  执行 `dotnet publish` 命令，生成 .exe 文件

## 引用

本项目使用了 `H.InputStimulator` 库

## 演示
![演示](./demo.gif)

## 开源协议
Do What The Fuck You Want To Public License
