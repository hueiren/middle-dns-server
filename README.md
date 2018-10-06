# 中間DNSサーバー
指定したドメインをブロックするDNSサーバー

  このアプリケーションを起動すると、DNSサーバーとして動きます。
  指定したドメインの名前解決をリクエストすると、IPアドレス0.0.0.0を返します。
  それ以外のドメインは、ネットワークアダプタに登録されたDNSサーバーに中継し、名前解決します。

# 設定(dns.iniの編集)

path = ファイル名

　　ブロックするドメインやIPアドレスを記述したファイルを指定します。

ipv4 = true

　　IPv4用DNSサーバーを起動する場合はtrueを指定します。起動しない場合はfalseを指定します。

ipv6 = true

　　IPv6用DNSサーバーを起動する場合はtrueを指定します。起動しない場合はfalseを指定します。

allow_ipv4 = 192.168.1.0/24

　　IPv4用DNSサーバーへのアクセスを許可するIPアドレスを指定します。サブネットマスクはCIDR表記です。

allow_ipv6 = fe80::/10

　　IPv6用DNSサーバーへのアクセスを許可するIPアドレスを指定します。サブネットマスクはCIDR表記です。

allow_ttl = 600

　　ブロックしない名前解決を行ったときの、IPアドレスの有効時間を秒単位で指定します。

block_ttl = 86400

　　ブロックする名前解決を行ったときの、IPアドレスの有効時間を秒単位で指定します。

# 注意事項

  DNSサーバーへのアクセスを許可するIPアドレスを限定することを推奨します。
  デフォルトの設定ではプライベートアドレスやリンクローカルアドレスのみ許可されます。


# 免責事項

  このアプリケーションを利用した事によるいかなる損害も作者は一切の責任を負いません。
  自己の責任の上で使用して下さい。