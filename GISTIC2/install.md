# GISTIC2安装  
> 目前的GISTIC2更新版本为2.0.23  (2017-03-27) 。  

## 下载  

```sh
wget -c ftp://ftp.broadinstitute.org/pub/GISTIC2.0/GISTIC_2_0_23.tar.gz
```

## 解压    

```shell
mkdir GISTIC2
mv GISTIC_2_0_23.tar.gz GISTIC2/ && cd GISTIC2/
tar zxf GISTIC_2_0_23.tar.gz
```

当前目录中包含  

```shell
~/download » ls                                                                             
examplefiles     GISTIC_2_0_23.tar.gz                  gp_gistic2_from_seg  MATLAB_Compiler_Runtime  refgenefiles
example_results  GISTICDocumentation_standalone_files  INSTALL.txt          MCR_Installer            run_gistic_example
gistic2          GISTICDocumentation_standalone.htm    LICENSE.txt          README.txt               source
```

## 安装matlab环境    

```shell
cd MCR_Installer/
unzip MCRInstaller.zip 
./install -mode silent -agreeToLicense yes -destinationFolder ~/software/GISTIC2/MATLAB_Compiler_Runtime/
```

## 配置环境变量  

```shell
echo "export XAPPLRESDIR=/home/ubuntu/software/GISTIC2/MATLAB_Compiler_Runtime/v83/X11/app-defaults:\$XAPPLRESDIR" >> ~/.zshrc
source ~/.zshrc
```

> 注意这里配置的文件是.zshrc，若使用的是bash，则为.bashrc  

## 运行GISTIC2示例文件：  

```shell
cd ../
./run_gistic_example
```



