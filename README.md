This a sub-repo of [Neard project](https://github.com/crazy-max/neard) involving Apache binary bundles.

## Installation

* Download and install [Neard](https://github.com/crazy-max/neard).
* If you already have installed Neard, stop it.
* Download [an Apache bundle](#download).
* Use a file archiver that supports [7z format](http://www.7-zip.org/7z.html) like [7zip](http://www.7-zip.org/) and extract the archive in `neard\bin\apache\`.

Directory structure example :
```
[-] neard
 | [-] bin
 |  | [-] apache
 |  |  | [-] apache2.2.22
 |  |     | neard.conf
 |  |  | [-] apache2.4.4
 |  |     | neard.conf
 ```

* Start Neard.
* Switch to the Apache version you have extracted on Neard (check [compatibility table](#compatibility-table) first) :

![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/switchVersion-20151214.png)

* If you have the warning icon on your Apache version, **you will have to switch the PHP version first**.

## Download

![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/star-20151214.png) : Default bundle on Neard.

### 2.2

|                   | Apache release date | Neard release | Download |
| ----------------- |:-------------------:|:-------------:|:--------:|
| **Apache 2.2.22** ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/star-20151214.png) | 2012/01/31 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.2.22-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.2.22-r1.zip) |
| **Apache 2.2.27** | 2014/03/18 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.2.27-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.2.27-r1.zip) |
| **Apache 2.2.29** | 2014/09/01 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.2.29-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.2.29-r1.zip) |
| **Apache 2.2.31** | 2015/07/16 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.2.31-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.2.31-r1.zip) |

### 2.4

|                   | Apache release date | Neard release | Download |
| ----------------- |:-------------------:|:-------------:|:--------:|
| **Apache 2.4.4**  | 2013/02/25 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.4.4-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.4.4-r1.zip) |
| **Apache 2.4.12** | 2015/01/27 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.4.12-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.4.12-r1.zip) |
| **Apache 2.4.17** | 2015/10/13 | [r1](https://github.com/crazy-max/neard-bin-apache/releases/tag/r1) | [neard-apache-2.4.17-r1.zip](https://github.com/crazy-max/neard-bin-apache/releases/download/r1/neard-apache-2.4.17-r1.zip) |
| **Apache 2.4.20** | 2016/04/11 | [r2](https://github.com/crazy-max/neard-bin-apache/releases/tag/r2) | [neard-apache-2.4.20-r2.7z](https://github.com/crazy-max/neard-bin-apache/releases/download/r2/neard-apache-2.4.20-r2.7z) |

## Compatibility table

|               | Apache 2.2.x  | Apache 2.4.x |
| ------------- |:-------------:|:------------:|
| **PHP 5.2.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ko-20151214.png) |
| **PHP 5.3.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) |
| **PHP 5.4.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) |
| **PHP 5.5.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ko-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) |
| **PHP 5.6.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ko-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) |
| **PHP 7.0.x** | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ko-20151214.png) | ![](https://raw.github.com/crazy-max/neard-bin-apache/master/img/ok-20151214.png) |

## Sources

* http://httpd.apache.org/
* http://www.apachehaus.com/

## Contribute

If you want to contribute to this bundle and create new bundles, you have to download [neard-dev](https://github.com/crazy-max/neard-dev) in the parent folder of the bundle.
Directory structure example :

```
[-] neard-dev
 | [-] build
 |  |  | build-commons.xml 
[-] neard-bin-apache
 |  | build.xml
```

To create a new bundle :
* Do not forget to increment the `build.release` in the `build.properties` file.
* If you want you can change the `build.path` (default `C:\neard-build`).
* Open a command prompt in your bundle folder and call the Ant target `release` : `ant release`.
* Upload your release on a file hosting system like [Sendspace](https://www.sendspace.com/).
* Create an [issue on Neard repository](https://github.com/crazy-max/neard/issues) to integrate your release.

## Issues

Issues must be reported on [Neard repository](https://github.com/crazy-max/neard/issues).<br />
Please read [Found a bug?](https://github.com/crazy-max/neard#found-a-bug) section before reporting an issue.
