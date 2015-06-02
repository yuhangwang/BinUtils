# BinUtils
**GNU BinUtils**

This is an unofficial verbatim redistribution of the binary&source form of the GNU BinUtils package under its open source license terms (see the LICENSE file).

This redistribution is under the same license as the original.

Please visit the official website for more details: http://www.gnu.org/software/binutils

## Download
You can download the compiled binary files at the [release page](https://github.com/yuhangwang/BinUtils/releases).

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
#### Version: 8.6.4
```bash
wget http://ftp.gnu.org/gnu/binutils/binutils-2.25.tar.gz
tar zxvf binutils-2.25.tar.gz
mkdir build_binutils-2.25
cd build_binutils-2.25
../binutils-2.25/configure --prefix=/home/steven/install/binutils/2.25--prefix=$target_dir --disable-nls --enable-build-warnings=yes --with-isl=/home/steven/install/isl/0.12.2 --with-cloog=/home/steven/install/cloog/0.18.0
make -j16
make -k check -j16 | tee QualityVerification.txt
make install
```

### Quality verification
See the "QualityVerification.txt" for the output of "make check".