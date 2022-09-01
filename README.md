# 此项目仅用作个人修复 clang-format

## 编译

1. `md build & cd build`
2. `cmake -G "Visual Studio 17 2022" -DCMAKE_BUILD_TYPE=Release -DLLVM_ENABLE_PROJECTS="clang" -DLLVM_ENABLE_ASSERTIONS=ON ..\llvm`
3. `msbuild tools\clang\tools\clang-format\clang-format.vcxproj /p:Configuration=Release -m`

然后你就能在 `build\Release\bin` 下找到编译好的 `clang-format.exe` 辣！
