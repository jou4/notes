## IE8のアドレスバーを非表示

レジストリに以下を登録

	HKEY_CURRENT_USER\Software\Policies\Microsoft\Internet Explorer\Toolbars\Restrictions
	DWORD値: NoNavBar = 1
