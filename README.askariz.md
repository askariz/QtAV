### QtAV 库学习
 安装依赖库
 ````
 sudo apt-get install libopenal-dev libpulse-dev libva-dev libxv-dev libass-dev libegl1-mesa-dev
 ````
 需要用到 Qt5Core Qt5Gui
 
 把该库当成正常库来使用,需要先sudo make install后才能使用qml 
 
### 如何使用该工程

 * 工程中涉及到使用qml 
    1. 首先该库在顶层CMakeLists中会先查找qml与quick的的相关库,如果找到了就会包含qml下的CMakeLists,该文件会生成QtAV的qml控件,需要提前安装到qml的搜索路径中
    2. 所有的.qml文件都包含在*.qrc中,这些都要包含在可执行文件的src中
    
    * 分析QMLPlayer的实现过程
        
    