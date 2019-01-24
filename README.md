# squirrel-config
### 配置内容
01. 外观
02. 过滤生僻字
03. Emoji
04. 颜文字
05. 英文输出
06. 中英混输
07. 符号输出
08. 修饰键输出
09. 各国货币英文缩写 (带提示)
10. 自定义短语
11. 缩写补全
12. 扩充词库
13. 输入状态切换
14. 部分 app 默认输出英文

### 相关说明
* **使用**

    除 `screenshot` 和 `README.md` 外，其它文件复制到 `用户设定...` 文件夹，选择 `重新部署`

* **外观**

    模仿 macOS 自带输入法外观，使用苹方字体，字体大小为 20，默认显示 5 个候选词，输入方案仅开启 `朙月拼音.简化字`
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/squirrel.png" alt="squirrel" height="72" />

* **生僻字**

    已对所有生僻字进行过滤，并对重复文字进行合并处理

* **Emoji**

    使用滤镜以避免 Emoji 被过滤，缺点是无法调频
    
    默认会和文字一起显示
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/emoji.png" alt="emoji" height="72" />
    
    可在开关选项中将其关闭
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/emoji-switch.png" alt="emoji-switch" height="72" />
    
    同时添加了 3 组 Emoji 快捷输出
    
    输入 `/bq` 显示所有表情
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/bq.png" alt="bq" height="72" />
    
    输入 `/ss` 显示所有手势
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/ss.png" alt="ss" height="72" />
    
    输入 `/am` 显示所有动物
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/am.png" alt="am" height="72" />
    
    因使用滤镜实现，所以同样无法调频，Emoji 快捷输出不受开关影响

* **颜文字**

    使用滤镜实现，无法调频，同样是为了避免被过滤，通过 [搜狗颜文字](https://pinyin.sogou.com/dict/ywz/) 提供的颜文字进行制作，并且加入了颜文字提示
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/kaomoji.png" alt="kaomoji" height="72" />
    
    如果需要关闭颜文字提示，将 `luna_pinyin_simp.custom.yaml` 文件中 `kaomoji-tips` 的 `reset: 1` 修改为 `reset: 0`，或者在 `reset: 1` 之后换行并加入可切换开关 `states: ["关闭颜文字提示", "开启颜文字提示"]`
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/kaomoji-turnoff-tips.png" alt="kaomoji-turnoff-tips" height="72" />
    
    为避免与其它调用关键词冲突，且考虑到颜文字较少使用，所以使用 `/v` 作为调用关键词的开头
    
    ```shell
    /vgx                    # 高兴
    /vmm                    # 卖萌
    /vmmd                   # 么么哒
    /vzj                    # 震惊
    /vsq                    # 生气
    /vwn                    # 无奈
    /vyun                   # 晕
    /vdq                    # 道歉
    /vdw                    # 动物
    /vhx                    # 害羞
    /vku                    # 哭
    /vsl                    # 睡啦
    /vbye                   # 再见
    /vaj                    # 傲娇
    /vch                    # 吃货
    /vdy                    # 得意
    /vhp                    # 害怕
    /vjiong                 # 囧
    /vzan                   # 赞
    /vng                    # 难过
    /vjian                  # 贱
    /vqt                    # 其它
    ```

* **英文输出 & 中英混输**

    词典来源网络，去除英文词典的词频调整，使英文排列在中文之后
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/easy-en.png" alt="easy-en" height="72" />
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/cn-en.png" alt="cn-en" height="72" />

* **符号输出**

    部分常用符号直接上屏，同时添加了 3 组符号快捷输出
    
    输入 `/fs` 显示常见分数
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/fs.png" alt="fs" height="72" />
    
    输入 `/fh` 显示常见符号
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/fh.png" alt="fh" height="72" />
    
    输入 `/xh` 显示常见星号
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/xh.png" alt="xh" height="72" />

* **修饰键输出**

    输入 `/aj` 或输入 `修饰键` 显示常见按键
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/aj.png" alt="aj" height="72" />
    
    同时可通过输入 `cmd` 输出 `⌘`、`ctrl` 输出 `⌃`
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/cmd.png" alt="cmd" height="72" />

* **各国货币英文缩写**

    通过滤镜实现了常见货币英文缩写，并且加入了提示，输入 `/hb` 显示常见货币
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/money.png" alt="money" height="72" />

* **自定义短语**

    在 `custom_phrase.txt` 文件中进行修改，如输入 `sj` 显示 `手机号码`、`gm` 显示 `Gmail 帐号`
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/custom-phrase.png" alt="custom-phrase" height="72" />

* **缩写补全**

    在 `luna_pinyin.i.dict.yaml` 文件中进行修改，如输入 `hk` 显示 `Hong Kong`、`smar` 显示 `Smartisan`、`sof` 显示 `Stack Overflow`
    
    <img src="https://github.com/grasonchan/squirrel-config/raw/master/screenshot/hk.png" alt="hk" height="72" />

* **扩充词库**

    转换自搜狗在线词库，部分词库来源网络
    
    如果要增删词库，在 `luna_pinyin.extended.dict.yaml` 文件中进行修改
    
    添加的个人词库包括 `luna_pinyin.i.dict.yaml` 和 `f_myphrases.dict.yaml`
    
    扩充的词库包括 `中英文混输`、`现代汉语常用词表`、`前端开发`、`互联网产品经理`、`知乎用户人名`、`网络流行新词`、`常见词汇`、`成语俗语`、`计算机词汇`、`开发专业词汇`、`热门电影`、`电视剧名`、`歌曲`、`最新流行歌曲专辑`、`明星`、`心理学词汇大全`

* **输入状态切换**

    * **中文输入状态**

      按 `Caps Lock ⇪` 键中文上屏并切换到 `大写英文` 输入状态，再按 `Caps Lock ⇪` 切换回 `中文` 输入状态；按 `Shift ⇧` 键英文上屏并切换到 `小写英文` 输入状态，再按 `Shift ⇧` 切换为 `中文` 输入状态

    * **小写英文输入状态**

      按 `Caps Lock ⇪` 键来回切换 `大小写英文`；按 `Shift ⇧` 键来回切换 `中英文`

* **部分 app 默认输出英文**

    * Finder
    * Spotlight
    * Launchpad (无法使用 `Shift ⇧` 进行中英文切换，如需切换使用 `Ctrl ⌃ + Shift ⇧ + 2` )
    * Safari
    * System Preferences
    * Terminal
    * Dictionary
    * Chrome
    * Firefox
    * Atom
    * VSCode
    * WebStorm
    * PhpStorm
    * Sketch
    * Photoshop
    * MacPass
    * AppCleaner
    * ShadowsocksX-NG-R8
    * Proxifier
    * Alfred