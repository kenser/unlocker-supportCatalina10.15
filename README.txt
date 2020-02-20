---<Manual(English)>--- 日本語は下(Japanese bottom)

For AMD CPU --> https://github.com/covolog/VMware-unlocker-forAMD
May be? AMD CPU CANNOT INSTALL Catalina10.15
+-----------------------------------------------------------------------------+
| IMPORTANT:   ONLY FOR VMware Workstation 15.5.0 or 15.5.1                   |
| ==========                                                                  |
|                                                                             |
| Don't remove or move files after installation!!!                            |
| You will not be able to uninstall.                                          |
+-----------------------------------------------------------------------------+
--Operation confirmed with--
Intel CPU (Core i7 8705G)
Windows 10, 64-bit  (Build 18363) 10.0.18363
macOS Catalina 10.15.4 beta
--------------------

--How To--
1. Install VMware Workstation first.
2. Extract files to any folder.

3. Windows
Explorer right click on the command file and select "Run as administrator".

win-install.cmd   - patches VMware
win-uninstall.cmd - restores VMware
--------------------
3. Linux
On Linux you will need to be either root or use sudo to run the scripts.
You may need to ensure the Linux scripts have execute permissions
by running chmod +x against the 2 files.

lnx-install.sh   - patches VMware
lnx-uninstall.sh - restores VMware
--------------------

4. restart the PC.
Create a Virtual machine on VMware.

5. Editing the VMX File.
If you did not specify location, look in Documents\virtual machines\
Right click on the VMX file and choose "Open with". Choose "More Apps".
From the list of apps that will be seen, choose "Notepad" and press Enter.
--For Intel CPU--
At the bottom add the code:

smc.version = "0"

Save the changes.

--Thanks--
Thanks to Dave Parsons for originally unlocker.


<----------------------------------------------------------------------------->

---<マニュアル(日本語 Japanese)>---

AMD CPU 用 --> https://github.com/covolog/VMware-unlocker-forAMD
多分？ AMD CPU は Catalina10.15 インストールできない。
+-----------------------------------------------------------------------------+
| 重要:   VMware Workstation 15.5.0 / 15.5.1 用                                |
| ==========                                                                  |
|                                                                             |
| インストール後にファイルを削除、移動しないでください。                           |
| アンインストールできなくなります。                                             |
+-----------------------------------------------------------------------------+
--動作確認済み--
Intel CPU (Core i7 8705G)
Windows 10, 64-bit  (Build 18363) 10.0.18363
macOS Catalina 10.15.4 beta
--------------------

--使い方--
1. まず VMware Workstation をインストール。
2. 任意の場所にファイルを展開。

3. Windows
コマンドファイルを右クリック、管理者として実行。

win-install.cmd   - VMware にパッチ
win-uninstall.cmd - VMware パッチを戻す
--------------------
3. Linux
Linuxでは、rootになるか、sudoを使用してスクリプトを実行する必要がある。
Linuxスクリプトに実行権限があるかの確認が必要。
2つのファイルに対してchmod + xを実行する。

lnx-install.sh   - VMware にパッチ
lnx-uninstall.sh - VMware パッチを戻す
--------------------

4. PC 再起動。
VMware で仮想マシンを作る。

5. VMX ファイルの編集。
初期フォルダは「Documents\virtual machines\」
VMX ファイルを右クリック、プログラムから開く->別のプログラムを選択->
メモ帳で開く。
--Intel CPU の場合--
コードを追加:

smc.version = "0"

上書き保存。

--サンクス--
オリジナル製作者、Dave Parsons 様に感謝いたします。
