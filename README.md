# Android Killer

> [!CAUTION] Windows Defender ��������
> 
>  ����һ����֪���� Android Killer �Լ� & Windows Defender �ļ����Ե��µ����⡣
>
> Android Killer ���� [legend_brother](https://www.52pojie.cn/home.php?mod=space&uid=366193) ������������ [52pojie](https://www.52pojie.cn/thread-319641-1-1.html) �� [pd521](https://www.pd521.com/thread-136-1-1.html) �� 2014 ~ 2015�����ʧ�ޣ�Ҳ���ڿ���֮��������һЩ���ڿ��ܻᱻ���Ϊ���������ԡ�
> 
> Windows Defender �ļ������������򹤾���Щ̫�ϸ��ˡ��Ƽ�ʹ�� [Kaspersky](https://www.kaspersky.com/) �� [����](https://www.huorong.cn/) ���� Windows Defender��������о���ʹ������ע����ȹ��ߵ����뱣��һ����ϵͳ��ȫ�ԵĻ���
> 
> ���� [VirusTotal](https://www.virustotal.com/gui/file/93816beef6269be75cc78f8c056cc4345e8e1263df2b34d65539d1650eb1e6cf) �ļ�������������ҹ�Ӧ����ʾ Android Killer �ǡ��������Ӷ��⡱�͡�Ǳ�ڵ�Σ�ա���
> 
> ���� [΢����ɳ��](https://s.threatbook.com/report/file/93816beef6269be75cc78f8c056cc4345e8e1263df2b34d65539d1650eb1e6cf) �ļ���������� Android Killer ���ǲ�����
> 
> ����㵣��ʹ�� Android Killer ��������Σ���������ǰ�� [52pojie](https://www.52pojie.cn/forum.php) ������Android Killer �����ĵط�֮һ��Ѱ������������򹤾ߡ�

> ע�⣺���ڼ�����ԭ�򣬱���Ŀʹ�� GB2312 �ַ�����

���ϲ��������������� Android �����빤�� ���� Android Killer��������ս 20 �꣡

˼·�ͷ������Դ���[��ҹ�ǳ� 2012](https://www.52pojie.cn/home.php?mod=space&uid=571540&do=profile&from=space) �� [AndroidKiller ��װ�����ü�ʹ�ý̳�](https://www.52pojie.cn/thread-726176-1-1.html)��

���߱Ͼ������ˣ������ǽ��滹�ǹ����϶��������⣬С���ڴ˻����Ƽ��͹ٳ��� JEB Decompiler 3 ������ά���� Android �����빤�ߡ�

## ʹ��

���[�˴�](../../archive/refs/heads/main.zip)��������ѹ��������ѹ���Ŀ¼��˫������ AndroidKiller.exe ���ɡ�

Android Killer ����ϸʹ�ý̳���[�ο�����](https://blog.csdn.net/yiran1919/article/details/132760445)������������

**ע�����ʹ�ñ�����ǰ������Ҫ�ڵ������ú� Java ���л�����**

## ��������

- `bin/`
  - ���� adb �� busybox���汾���ˣ����þ��У�������˵ ?��
  - ���� apktool.jar �� v2.11.1
  - ���� dex2jar �� v2.4
  - ���� Android Killer ���õ� jd-gui��ʹ���Լ���д���м���� [android-killer-jadx-gui-support](../../../android-killer-jadx-gui-support) ������ת���� jadx-gui
- `tools/`
  - ��� [ApkScan PKID](http://www.legendsec.org/1888.html) ��ǹ��ߣ����������Զ��Ч���޷���֤������Ѱ�����������
  - ��� [InjectLog](https://www.52pojie.cn/thread-743758-1-1.html) ��־���ߣ��ּ� [Android Ӧ�����򡪡��������������֮������](https://blog.csdn.net/charlessimonyi/article/details/52027563)
  - ��� jadx-gui ������ jre �汾�������� v1.4.7��GitHub �ϴ����ļ�������� 100MB��v1.5.0+ �汾���ޣ������и�����Ҫ���볢��[���и���](#jadx-gui-���·���)��

## ���и���

### apktool ���·���

1. �� [apktool ����ҳ��](https://github.com/iBotPeaches/Apktool/releases) �������°�� `apktool_x.x.x.jar`
2. ������ `bin/apktool/apktool/` Ŀ¼�£��� **Android Killer** ��ҳ�� **Android** �˵����� **APKTOOL ������**��������صİ汾������ΪĬ��

   ![չʾ](docs/images/image1.png)
   ![չʾ](docs/images/image2.png)

### dex2jar ���·���

1. �� [dex2jar ����ҳ��](https://github.com/pxb1988/dex2jar/releases) �������°�� `dex-tools-xxx.zip`���ɰ���Ϊ `dex2jar-xxx.zip`��
2. ��� `bin/dex2jar/` Ŀ¼���ļ��������صõ���ѹ��������ȫ����ѹ������Ŀ¼

### jadx-gui ���·���

1. �� [jadx ���ؽ���](https://github.com/skylot/jadx/releases) �������°�� `jadx-gui-x.x.x-win.zip`���ɰ�Ϊ `jadx-gui-x.x.x-no-jre.exe`��
2. ��ѹ�������ݽ�ѹ�� `tools/JadxGui/` Ŀ¼�£������� `jadx-gui-x.x.x.exe` Ϊ `jadx-gui.exe`�����Ǿɰ棨�ɰ�ֱ����������ִ�г��򣬺󸲸Ǽ��ɣ�

## ע������ & һЩ����

- ����Ӧ��ʱ�빴ѡ AndroidKiller ǩ�������������� apk �ļ����ʲ�������ʹ��
- �����װ���� "Failure [INSTALL_FAILED_INVALID_APK: Failed to extract native libraries, res=-2]"�� �뽫 `AndroidManifest.xml` �ļ��е� `extractNativeLibs=false` �޸�Ϊ `extractNativeLibs=true`���ٴγ���
