# はじめてのPerl6

https://perl6.org/

## 用語

**Perl6**:
言語仕様とテストスイート。

**Rakudo**:
Perl6コンパイラ。

**Rakudobrew**:
Rakudoインストールマネージャ。

**Panda**:
モジュールインストーラ。

**Rakudo Star**:
Rakudo、Panda、モジュールとドキュメントのセット。

## インストール

インストール手順は次のとおりです。添付のVagrantfileも参考にしてください。

1. Rakudobrewのインストール
2. Rakudoのインストール（MoarVM）
3. Pandaのインストール
4. Task::Starのインストール

Windowsでは[こちら](http://rakudo.org/downloads/star/)にあるインストーラを利用してインストールできます。

OSXでは`brew install rakudo-star`でインストールできます。

## 実行

perl6では標準でREPLが提供されます。

```
$ perl6
> say "Hello Perl6"
Hello Perl6
```

ファイルから実行する場合は次のように引数にファイルパスを渡します。

ファイルの拡張子は`.pl`、`.pm`です。
Perl6で書かれていることを強調したい場合は`.p6`、`.pm6`を使用します。

http://doc.perl6.org/language/modules

```
$ cat <<EOF > hello.p6
say "Hello Perl6";
EOF
$ perl6 hello.p6
Hello Perl6
```

## ドキュメント

* [Perl 6 Language Documentation](https://doc.perl6.org/language.html)
* [Perl 6 Types](https://doc.perl6.org/type.html)
* [Perl 6 Routines](https://doc.perl6.org/routine.html)

## モジュール

* [Perl 6 Modules Directory](https://modules.perl6.org/)

## 勉強会

* [第1回](01.md)
