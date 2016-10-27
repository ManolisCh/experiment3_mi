# experiment3_mi
repo for the third experiment using MI

# Installing fuzzylite cpp library 

1) Download the v4.0 library
2) unzip the source code in order to build nd install library
3) cd into the fuzzylite folder
4) change the code in CMakeLists.txt file into:
```sh
install(TARGETS fl-bin fl-shared fl-static
		RUNTIME DESTINATION bin
		LIBRARY DESTINATION lib
		ARCHIVE DESTINATION lib
		)
```

5) run the following commands
```sh
$ mkdir -p release
$ cmake -G"Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DFL_BACKTRACE=ON -DFL_USE_FLOAT=OFF -DFL_CPP11=ON
$ make
$ sudo make install
```

6) the library should work
