## IE8のアドレスバーを非表示

レジストリに以下を登録

	HKEY_CURRENT_USER\Software\Policies\Microsoft\Internet Explorer\Toolbars\Restrictions
	DWORD値: NoNavBar = 1

## IP設定コマンド

DHCP

    netsh interface ip set address <interface name> dhcp
    netsh interface ip set dns <interface name> dhcp

    netsh interface ip set address "ワイヤレス ネットワーク接続" dhcp
    netsh interface ip set dns "ワイヤレス ネットワーク接続" dhcp

固定IP

    netsh interface ip set address <interface name> static <ip> <mask> <gateway>
    netsh interface ip set dns <interface name> static <ip> primary
    netsh interface ip add dns <interface name> <ip>

    netsh interface ip set address "ワイヤレス ネットワーク接続" static 136.131.21.86 255.255.255.0 136.131.21.241
    netsh interface ip set dns "ワイヤレス ネットワーク接続" static 133.189.49.230 primary
    netsh interface ip add dns "ワイヤレス ネットワーク接続" 133.189.150.111

インターフェース名等の確認

    netsh interface ip show config

