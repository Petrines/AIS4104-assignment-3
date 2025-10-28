### How to setup vcpkg (in manifest mode)

Call CMake with `-DCMAKE_TOOLCHAIN_FILE=C:/vcpkg/scripts/buildsystems/vcpkg.cmake`

Add optional features by listing them with `-DVCPKG_MANIFEST_FEATURES=feature1;feature2`

See [vcpkg.json](../../../../Workspace/AIS4104-assignment/vcpkg.json) for available features.

Note, however, that under MinGW you'll need to specify the vcpkg triplet:
```shell
-DVCPKG_TARGET_TRIPLET=x64-mingw-[static|dynamic]  # choose either `static` or `dynamic`.
-DVCPKG_HOST_TRIPLET=x64-mingw-[static|dynamic]    # <-- needed only if MSVC cannot be found. 
```
Source: [threepp](https://github.com/markaren/threepp/blob/master/vcpkg.json).

## How to use git
```bash
git add --all
git commit -m "This is my message"
git push origin master
```

## Correct VCPKG.json contents

```json
{
  "$schema" : "https://raw.githubusercontent.com/microsoft/vcpkg/master/scripts/vcpkg.schema.json",
  "name" : "test",
  "dependencies" : [
    "eigen3"
  ]
}
```