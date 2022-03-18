# MesonPractice

https://mesonbuild.com/

```sh
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple meson
手动下载 https://github.com/ninja-build/ninja/releases

$ meson --version
0.61.3
$ ninja --version
1.10.2

$ meson --help
```


```sh
# 常用编译步骤
$ cd /path/to/source/root
$ meson builddir && cd builddir
$ meson compile
$ meson test
```

It is recommended that you keep one build directory for unoptimized builds and
one for optimized ones. To compile any given configuration, just go into the
corresponding build directory and run meson compile.


```sh
$ cd /path/to/source/root
$ meson --prefix /usr --buildtype=plain builddir -Dc_args=... -Dcpp_args=... -Dc_link_args=... -Dcpp_link_args=...
$ meson compile -C builddir
$ meson test -C builddir
$ DESTDIR=/path/to/staging/root meson install -C builddir
```

