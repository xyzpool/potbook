#IDEA快捷操作
---
		查找工程内JAVA文件:ctrl+n
		查找工程内文件:ctrl+shift+n  
		全局查找:ctrl+shift+f  
		全局替换:ctrl+shift+r  
		Link with editor功能:项目导航栏点击右上角设置，勾选Auto scroll from source
		查看方法被引用的快捷方式:alt+F7
		查找上一次/下一次查看的地址:ctrl+shift+left/right
		查找接口/实现类:ctrl+b / ctrl+shift+b
		
		
   
#MAVEN依赖管理
---
		构建中批量修改同一工程版本号:
		mvn version:set -DartifactId=artifactId -DnewVersion=%新 版本号%
		新版本号不正确时撤销新的版本号:
		mvn versions:revert
		
		确认新版本号无误后提交新版本号设置:
		mvn versions:commit;