# 学習メモ
課題の中で調べたことなどをまとめる

## 使われている関数
```c
/**
 * ストリームのバッファの設定を行う関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man3/setbuf.3.html
 */
void setbuf(FILE *stream, char *buf);

/**
 * 通信のエンドポイントを作成し、エンドポイントを表すソケット記述子を返す関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man2/socket.2.html
 */
int socket(int *domain, int type, int protocol);

/**
 * ソケットと関連したオプションを設定する関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man2/setsockopt.2.html
 */
int setsockopt(int socket, int level, int option_name, const void *option_value, socklen_t option_len);

/**
 * ソケットに名前をつける関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man2/bind.2.html
 */
int bind(int socket, const struct sockaddr *address, socklen_t address_len);

/**
 * ソケット上の接続を待つ関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man2/listen.2.html
 */
int listen(int socket, int backlog);

/**
 * ソケットへの接続を受ける関数
 * ref: https://linuxjm.osdn.jp/html/LDP_man-pages/man2/accept.2.html
 */
int accept(int socket, struct sockaddr *restrict address, socklen_t *restrict address_len);
```

## 参考リンク
[ストリームとファイル記述子の違い](https://www.gnu.org/software/libc/manual/html_node/Streams-and-File-Descriptors.html)

[ソケット通信を行うサーバープログラムの全体像](http://research.nii.ac.jp/~ichiro/syspro98/server.html)
