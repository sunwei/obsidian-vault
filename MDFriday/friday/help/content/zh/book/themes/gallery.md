# Gallery 主题
## 1.主题概述
**Gallery** 是一款专为展示图片、摄影作品和艺术创作设计的主题，旨在帮助用户轻松快捷地创建视觉效果令人惊艳的网站。它提供了简洁、优雅的设计，完美呈现您的图片和视觉内容。

![gallery](gallery-home.jpg)
### **适用场景**

- **摄影作品集网站**：非常适合摄影师展示个人作品和精选摄影集。
- **艺术作品集网站**：为艺术家、插画师和设计师提供一个展示艺术创作和设计作品的平台。
- **个人博客**：为创作者提供一个展示作品、分享经验和故事的美丽布局。
- **活动或展览网站**：适合展示活动照片、展览或画廊内容。
- **在线艺术画廊**：艺术家或艺术机构可用此主题展示和销售艺术作品。
- **公司作品集**：视觉导向型的公司可以使用此主题展示产品摄影、品牌设计及其他创意项目。

### **主要特点**

- **极简设计**：简洁优雅的布局，聚焦于图片和内容的展示。
- **响应式设计**：自动适配各种屏幕尺寸，确保在桌面、平板和手机设备上都有良好的浏览体验。
- **图像为主**：特别针对大图展示，提供网格和灯箱格式以突显视觉内容。
- **Markdown 内容管理**：无需编码知识，轻松使用 Markdown 文件管理内容和图片。
- **模块化内容**：按需展示作品集、关于我们、联系方式等内容，井然有序。
- **SEO 优化**：内置 SEO 优化功能，助力网站在搜索引擎中获得更高排名。
- **快速轻量**：针对性能进行优化，保证快速加载和流畅的浏览体验。

该主题非常适合任何希望创建一个以视觉内容为主的网站，帮助您轻松展示和分享创作。

## 2. 在线演示

- 请访问 [Gallery 主题在线演示](https://theme-gallery.sure40.com/) 查看主题效果。

## 3. 示例目录结构


```plaintext
.
├── Gallery Demo.md                # 演示页面：展示图库示例的 Markdown 文件
├── theme-gallery                  # 主题目录：包含主题相关文件和内容
│   ├── README.md                  # 主题说明：介绍该主题及其使用方法
│   ├── content                    # 内容文件夹：包含实际页面内容的 Markdown 文件和资源
│   │   ├── _index.md              # 主页：主题的首页内容
│   │   ├── about.md               # 关于我们：介绍公司或网站的信息
│   │   ├── animals                # 动物相关页面：包含不同类别的动物图像
│   │   │   ├── _index.md          # 动物主页：展示所有动物类别的索引页
│   │   │   ├── cats               # 猫类：展示猫相关内容的子目录
│   │   │   │   ├── alexander-london-mJaD10XeD7w-unsplash.jpg  # 猫咪图片
│   │   │   │   ├── amber-kipp-75715CVEJhI-unsplash.jpg       # 猫咪图片
│   │   │   │   ├── bogdan-farca-CEx86maLUSc-unsplash.jpg      # 猫咪图片
│   │   │   │   ├── edgar-nKC772R_qog-unsplash.jpg             # 猫咪图片
│   │   │   │   ├── index.md         # 猫类页面：展示猫类的更多信息
│   │   │   │   ├── kabo-p6yH8VmGqxo-unsplash.jpg             # 猫咪图片
│   │   │   │   ├── manja-vitolic-gKXKBY-C-Dk-unsplash.jpg    # 猫咪图片
│   │   │   │   ├── michael-sum-LEpfefQf4rU-unsplash.jpg      # 猫咪图片
│   │   │   │   └── raoul-droog-yMSecCHsIBc-unsplash.jpg       # 猫咪图片
│   │   │   ├── dogs               # 狗类：展示狗相关内容的子目录
│   │   │   │   ├── charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg   # 狗狗图片
│   │   │   │   ├── index.md         # 狗类页面：展示狗类的更多信息
│   │   │   │   ├── milli-2l0CWTpcChI-unsplash.jpg            # 狗狗图片
│   │   │   │   ├── richard-brutyo-Sg3XwuEpybU-unsplash.jpg    # 狗狗图片
│   │   │   │   └── taylor-kopel-WX4i1Jq_o0Y-unsplash.jpg     # 狗狗图片
│   │   │   └── janis-ringli-UC1pzyJFyvs-unsplash.jpg          # 动物图片
│   │   ├── fashion-beauty         # 时尚与美容：展示时尚和美容类别的图片
│   │   │   ├── harper-sunday-FkxXePJJH5g-unsplash.jpg         # 时尚图片
│   │   │   ├── index.md            # 时尚与美容页面：介绍时尚与美容的更多内容
│   │   │   ├── kamil-kalkan-7gqnlnCTvlg-unsplash.jpg          # 时尚图片
│   │   │   ├── laura-chouette-63obHScZWZw-unsplash.jpg         # 时尚图片
│   │   │   └── mina-rad-V94CguEmeos-unsplash.jpg               # 时尚图片
│   │   ├── featured-album         # 精选专辑：展示精选相册的页面
│   │   │   ├── index.md            # 精选专辑主页：展示精选专辑内容
│   │   │   ├── jeremy-bishop-pjszS6Q2g_Y-unsplash.jpg          # 专辑图片
│   │   │   └── manny-becerra-IFlBNNOLHUo-unsplash.jpg          # 专辑图片
│   │   ├── links.md               # 外部链接：展示相关外部资源或链接
│   │   ├── martin-martz-wRuhOOaG-Z4-unsplash.jpg               # 图片资源
│   │   ├── nature                 # 自然：展示自然相关的图片
│   │   │   ├── azzedine-rouichi-ZS_XuDZmxpM-unsplash.jpg       # 自然风光图片
│   │   │   ├── azzedine-rouichi-f_C_lFxqThI-unsplash.jpg       # 自然风光图片
│   │   │   ├── enyioma-adu-RuaRTaKi-D4-unsplash.jpg            # 自然风光图片
│   │   │   ├── francesco-ungaro-P45gR9kH0SM-unsplash.jpg       # 自然风光图片
│   │   │   ├── index.md            # 自然页面：展示自然相关内容
│   │   │   ├── isaac-wolff-k_PbdrEs79g-unsplash.jpg             # 自然风光图片
│   │   │   ├── veronica-wu-4f8u5mFGKjw-unsplash.jpg            # 自然风光图片
│   │   │   ├── vitalik-vynarchyk-TUzsO59UFpo-unsplash.jpg      # 自然风光图片
│   │   │   ├── wolfgang-hasselmann-U7BG3FOT5r8-unsplash.jpg     # 自然风光图片
│   │   │   └── wolfgang-hasselmann-x7CyIC2jUaE-unsplash.jpg     # 自然风光图片
│   │   ├── private                # 私密：展示私密和个性化内容的图片
│   │   │   ├── eugene-golovesov-6dH1__uRYtg-unsplash.jpg       # 私密图片
│   │   │   ├── eugene-golovesov-gRknIewfaBs-unsplash.jpg       # 私密图片
│   │   │   ├── index.md            # 私密页面：展示私密内容
│   │   │   ├── kiona-_lQgFjsTgEs-unsplash.jpg                  # 私密图片
│   │   │   ├── ruan-richard-rodrigues-t2WImwH1Fa0-unsplash.jpg  # 私密图片
│   │   │   ├── urja-bhatt-QQ0naV2n-mg-unsplash.jpg             # 私密图片
│   │   │   └── wolfgang-hasselmann-7pYqHNp37Pg-unsplash.jpg    # 私密图片
│   │   └── social                 # 社交：展示社交媒体相关内容
│   │       ├── social1.md         # 社交页面 1：社交媒体内容
│   │       ├── social10.md        # 社交页面 2：社交媒体内容
│   │       ├── social11.md        # 社交页面 3：社交媒体内容
│   │       ├── social2.md         # 社交页面 4：社交媒体内容
│   │       ├── social3.md         # 社交页面 5：社交媒体内容
│   │       ├── social4.md         # 社交页面 6：社交媒体内容
│   │       ├── social5.md         # 社交页面 7：社交媒体内容
│   │       ├── social6.md         # 社交页面 8：社交媒体内容
│   │       ├── social7.md         # 社交页面 9：社交媒体内容
│   │       ├── social8.md         # 社交页面 10：社交媒体内容
│   │       └── social9.md         # 社交页面 11：社交媒体内容
│   └── manifest.json             # 主题配置文件：包含主题设置和配置参数
```

在此目录结构中，注释解释了各个目录和文件的用途。每个子目录和文件都对应特定的内容部分或资源，方便管理和展示不同类型的图片、文章和社交媒体内容。


## 4. 如何使用 Gallery 主题

### 步骤指南：

1. **更换主题**：修改文件中的 `theme` 字段为 `github.com/mdfriday/theme-gallery`。
```plaintext
friday-plugin: enabled
site: '0'
theme: github.com/mdfriday/theme-hero
project: empty
defaultLanguage: en
ga: GT-XXXXXXXXX
```

将 `theme` 行修改为：

```plaintext
theme: github.com/mdfriday/theme-gallery
```

2. **下载样例文件**：从 MDFriday 下载 Gallery 主题的样例文件，并保存到本地。
3. **编辑文件**：打开样例文件，修改图片、文本和社交媒体链接等内容，以符合您的个人或专业需求。
4. **预览网站**：在本地预览更改，确保一切显示正常。
5. **发布画廊**：当您对预览效果满意后，部署网站并开始展示您的作品。

这个主题为任何希望创建以视觉内容为主的网站的用户提供了一个极好的起点。它易于使用、高度可定制，并且完美适用于展示创作作品的创作者、艺术家和设计师。