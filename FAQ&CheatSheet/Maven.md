# Maven FAQ

### Maven 打包发布到Nexus服务器

%var1%当前版本号
mvn versions:set -DnewVersion=%var1%-SNAPSHOT
mvn clean source:jar deploy -Dmaven.test.skip = true
mvn versions:revert
mvn versions:commit

nexus服务器有SNAPSHOT开发服务器和发布服务器之分.
发布服务器一个版本号只能上传一次,且不能重复上传
开发服务器可以重复上传,但是必须以SNAPSHOT结束