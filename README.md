# ExampleAsio
Using Boost.Asio with CMake

### Building Boost 1.64 with Visual Studio 2015 ###

```sh
bootstrap.bat

b2 -j8 toolset=msvc-14.0 address-model=32 architecture=x86 link=static threading=multi runtime-link=shared --build-type=minimal stage --stagedir=stage/win32
```