MeCab
=====

This fork exists solely to make mecab easier to install.
I've also renamed the gem from mecab-ruby-gem to just mecab.
I don't take any credit for this gem.

Original is at https://github.com/hotchpotch/mecab-ruby-gem

Example Usage
=============
```ruby
require 'mecab'

sentence = "太郎はこの本を二郎を見た女性に渡した。"
tagger = MeCab::Tagger.new
puts tagger.parse sentence

太郎	名詞,固有名詞,人名,名,*,*,太郎,タロウ,タロー
は	助詞,係助詞,*,*,*,*,は,ハ,ワ
この	連体詞,*,*,*,*,*,この,コノ,コノ
本	名詞,一般,*,*,*,*,本,ホン,ホン
を	助詞,格助詞,一般,*,*,*,を,ヲ,ヲ
二	名詞,数,*,*,*,*,二,ニ,ニ
郎	名詞,一般,*,*,*,*,郎,ロウ,ロー
を	助詞,格助詞,一般,*,*,*,を,ヲ,ヲ
見	動詞,自立,*,*,一段,連用形,見る,ミ,ミ
た	助動詞,*,*,*,特殊・タ,基本形,た,タ,タ
女性	名詞,一般,*,*,*,*,女性,ジョセイ,ジョセイ
に	助詞,格助詞,一般,*,*,*,に,ニ,ニ
渡し	動詞,自立,*,*,五段・サ行,連用形,渡す,ワタシ,ワタシ
た	助動詞,*,*,*,特殊・タ,基本形,た,タ,タ
。	記号,句点,*,*,*,*,。,。,。
EOS

```
Installation
============
```
gem install mecab
```

Installing prerequisites
=============

* Mecab (0.996)
* mecab-ipadic

# Homebrew

```
$ brew update
$ brew install mecab mecab-ipadic
```

# Unix

```
curl https://mecab.googlecode.com/files/mecab-0.996.tar.gz
tar zxf mecab-0.996.tar.gz
cd mecab-0.996
./configure --with-charset=utf8 --enable-utf8-only
make
sudo make install
```
