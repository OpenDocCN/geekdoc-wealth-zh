# PHP 备忘单[更新] -下载 PDF 快速参考

> 原文：<https://hackr.io/blog/php-cheat-sheet>

### **变量处理功能**

PHP 中的变量是存储数据的容器。

*   变量名前面有一个＄符号。
*   它必须以变量或下划线开头。
*   变量不能以数字开头。
*   变量只能包含字母数字字符。
*   变量区分大小写。$Result 和$result 被视为两个不同的变量。

可变函数允许我们根据需要定义、使用和操作变量。

| 1.  | 钻头选择 | 返回变量的布尔值。 |
| 2.  | debug_zval_dump | 将内部 zend 值的字符串表示转储到输出。 |
| 3. | 双 val | 浮舟的别名。 |
| 4. | 清空 | 确定变量是否为空。 |
| 5. | 浮动 | 返回变量的浮点值。 |
| 6. | 获取已定义变量 | 返回所有已定义变量的数组。 |
| 7. | 获取资源类型 | 返回资源类型。 |
| 8. | gettype | 返回变量的类型。 |
| 9. | 导入请求变量 | 将 GET/POST/Cookie 变量导入资源类型。 |
| 10. | 巧合 | 获取变量的整数值。 |
| 11. | is_array | 确定变量是否为数组 |
| 12. | is_bool | 确定变量是否为布尔型 |
| 13. | 是 _ 可调用的 | 验证变量的内容是否可以被称为函数。 |
| 14. | is _ float &#124; is double &#124; is _ real | 确定变量的类型是否为“浮点”。 |
| 15. | is _ int &#124; is _ integer &#124; is _ long | 确定变量的类型是否为整数。 |
| 16. | is_null | 确定变量是否为空 |
| 17. | 是 _ 数字 | 确定变量是数字还是数字串。 |
| 18. | is_object | 确定一个变量是否是一个对象。 |
| 19. | is_resource | 确定一个变量是否是资源。 |
| 20. | 是 _ 标量 | 确定变量是否是标量。 |
| 21. | is_string | 确定变量的类型是否为字符串。 |
| 22. | isset | 确定一个变量是否被设置且不为空。 |
| 23. | 打印 _r | 以人类可读的格式打印信息。 |
| 24. | 连载 | 生成一个值的可存储表示。 |
| 25. | 设置类型 | 设置变量的类型。 |
| 26. | 梁 | 获取变量的字符串值。 |
| 27. | 取消序列化 | 创建一个存储变量的 PHP 值。 |
| 28. | 未置位 | 取消给定变量的设置 |
| 29. | var_dump | 转储关于变量的信息。 |
| 30. | var_export 的缩写形式 | 输出或返回变量的可解析字符串表示。 |

### **数组函数**

一个数组用来在一个变量中存储一系列的值。这些值可以通过引用一个总是从 0 开始的索引号来访问。数组可以是:

*   **索引:**默认数组格式。可以通过索引号访问值。
*   **关联:**使用命名键。
*   **多维:**也可称为矩阵。它包含一个或多个数组。你也可以把它想象成一个嵌套的数组。

数组函数允许我们根据需要定义、存储、遍历数据和信息。

| 1. | 数组() | 声明并创建一个数组。 |
| 2. | 数组 _ 变化 _ 关键字 _ 案例() | 返回一个包含所有小写或大写键的数组。 |
| 3. | array_chunk() | 将一个数组分割成数组块。 |
| 4. | array_combine() | 使用一个键数组和一个值数组创建一个数组。 |
| 5. | 数组计数值() | 返回一个数组，其中包含每个值出现的次数。 |
| 6. | array_diff() | 比较数组值并返回差值。 |
| 7. | array_diff_assoc() | 比较数组键和值并返回差异。 |
| 8. | array_diff_key() | 比较数组键并返回差异。 |
| 9. | array _ diff _ uassoc() | 将数组的键和值与用户进行的额外函数检查进行比较，并返回差异。 |
| 10. | array_diff_ukey() | 将数组键与用户进行的额外函数检查进行比较，并返回差异。 |
| 11. | array_fill() | 用值填充数组。 |
| 12. | array_filter() | 通过用户自定义函数过滤数组元素。 |
| 13. | array_flip() | 交换数组中所有键及其相关值。 |
| 14. | array_intersect() | 比较数组值并返回匹配结果 |
| 15. | array_intersect_assoc() | 比较数组的键和值，并返回匹配结果。 |
| 16. | 数组 _ 交集 _ 关键字() | 比较数组键并返回匹配项。 |
| 17. | array_intersect_uassoc() | 比较键和值，使用额外的用户自定义函数检查并返回匹配项。 |
| 18. | array_intersect_ukey() | 比较密钥，使用额外的用户自定义函数检查并返回匹配结果。 |
| 19. | 数组 _ 关键字 _ 存在() | 确定指定的键是否存在于数组中。 |
| 20. | array_keys() | 返回一个数组的所有键。 |
| 21. | array_map() | 将数组中的每个值发送给用户自定义的函数，该函数返回新值。 |
| 22. | 数组 _ 合并()&#124;数组 _ 合并 _ 递归() | 将一个或多个数组合并成一个数组。 |
| 23. | array_multisort() | 对多维数组进行排序。 |
| 24. | array_pad() | 向数组中插入指定数量和指定值的项。 |
| 25. | array_pop() | 删除数组的最后一个元素。 |
| 26. | array_product() | 计算数组中数值的乘积。 |
| 27. | array_push() | 在数组末尾插入一个或多个元素。 |
| 28. | array_rand() | 从数组中返回一个或多个随机键。 |
| 29。 | array_reduce() | 使用用户定义的函数，以字符串形式返回数组。 |
| 30. | array_reverse() | 以相反的顺序返回一个数组。 |
| 31. | array_search() | 在数组中搜索给定值并返回键。 |
| 32. | array_shift() | 从数组中移除第一个元素，并返回被移除元素的值。 |
| 33. | array_slice() | 移除并替换数组中的指定元素。 |
| 34. | array_splice() | 移除并替换数组中的指定元素 |
| 35. | array_sum() | 返回数组中数值的总和。 |
| 36. | array_udiff() | 比较用户自定义函数中的数组值并返回一个数组。 |
| 37. | array_udiff_assoc() | 比较数组键，比较用户自定义函数中的数组值，返回一个数组。 |
| 38. | array _ udiff _ uassoc() | 比较用户自定义函数中的数组键和数组值，返回一个数组。 |
| 39. | array _ ui intersect() | 比较用户自定义函数中的数组值并返回一个数组。 |
| 40. | array_uintersect_assoc() | 比较数组键，比较用户自定义函数中的数组值，返回一个数组。 |
| 41. | array _ uintersect _ UAS SOC() | 比较数组键和数组值是用户自定义函数，并返回一个数组。 |
| 42. | array_unique() | 从数组中删除重复值。 |
| 43. | array_unshift() | 将一个或多个元素添加到数组的开头。 |
| 44. | array_values() | 返回一个数组的所有值。 |
| 45. | array_walk() | 将用户函数应用于数组的每个成员。 |
| 46. | array_walk_recursive() | 将用户函数递归应用于数组的每个成员。 |
| 47. | arsort() | 对数组进行逆序排序，并保持索引关联。 |
| 48. | asort() | 对数组排序并维护索引关联。 |
| 49. | 紧凑() | 创建包含变量及其值的数组。 |
| 50. | count() | 对数组中的元素或对象中的属性进行计数。 |
| 51. | 当前() | 返回数组中的当前元素 |
| 52. | 各() | 从数组中返回当前的键和值对 |
| 53. | end() | 将数组的内部指针设置为指向它的最后一个元素。 |
| 54. | 提取() | 从数组导入变量到当前符号表。 |
| 55. | in_array() | 检查数组中是否存在指定的值。 |
| 56. | 键() | 从数组中取出一个键。 |
| 57. | krsort() | 按逆序对数组进行排序。 |
| 58. | ksort() | 按键对数组排序。 |
| 59. | 列表() | 给变量赋值，就像它们是一个数组。 |
| 60. | natcasesort() | 使用不区分大小写对数组进行排序。 |
| 61. | natsort() | 对数组进行排序 |
| 62. | 下一个() | 将数组的内部数组指针前移 |
| 63. | pos() | 当前的别名。 |
| 64. | prev() | 倒回内部数组指针。 |
| 65. | 范围() | 创建一个包含一系列元素的数组。 |
| 66. | 复位() | 设置一个数组的内部指针指向它的第一个元素。 |
| 67. | rsort() | 对数组进行逆序排序。 |
| 68. | 洗牌() | 打乱一个数组 |
| 69. | sizeof() | count()的别名 |
| 70. | sort() | 对数组进行排序 |
| 71. | uasort() | 使用自定义函数对数组进行排序，并维护索引关联。 |
| 72. | uksort() | 使用用户定义的函数按关键字对数组进行排序 |
| 73. | usort() | 使用用户定义的函数按值对数组排序。 |

### **数组常数**

| 1. | CASE_LOWER | 与 array_change_key_case()一起使用，将数组键转换成小写 |
| 2. | 案例 _ 上位 | 与 array_change_key_case()一起使用，将数组键转换为大写 |
| 3. | SORT_ASC | 与 array_multisort()一起使用，按升序排序 |
| 4. | 排序 _DESC | 与 array_multisort()一起使用，按降序排序 |
| 5. | 排序 _ 常规 | 用于正常比较项目 |
| 6. | 排序 _ 数值 | 用于从数字上比较项目 |
| 7. | 排序 _ 字符串 | 用于比较字符串形式的项目 |
| 8. | SORT_LOCALE_STRING | 用于根据当前区域设置将项目作为字符串进行比较 |
| 9. | 计数 _ 正常 | 计算数组中的所有元素。 |
| 10. | 计数 _ 递归 | 递归计算数组中的元素。 |
| 11. | EXTR_OVERWRITE | 将数组中的变量导入到当前符号表中。 |
| 12. | EXTR_SKIP | 这是一面拔旗。如果有冲突，不要覆盖现有变量。 |
| 13. | EXTR_PREFIX_SAME | 如果有冲突，在变量名前加上 **前缀** 。 |
| 14. | xtr _ prefix _ all | 所有变量名前加 **前缀** 。 |
| 15. | 提取前缀无效 | 只用 **前缀** 作为无效/数值变量名的前缀。 |
| 16. | 提取前缀如果存在 | 只有当前符号表中存在相同变量的非前缀版本时，才创建带前缀的变量名。 |
| 17. | 外部条件存在 | 如果变量已经存在于当前符号表中，则只覆盖该变量，否则不做任何操作。这对于定义一个有效变量列表，然后只提取那些在$_REQUEST 中定义的变量非常有用。 |
| 18. | EXTR_REFS | 提取变量作为参考。这意味着导入变量的值仍然引用数组参数的值。 |

### **字符串函数**

字符串是一系列字符。它是一种数据类型。它也可以是字母数字。字符串是通过声明一个变量并给它分配字符串来创建的。字符串函数允许我们根据需要操纵和处理字符串。

| 1. | addcslages() | 返回在指定字符前面带有反斜杠的字符串。 |
| 2. | addslashes() | 返回预定义字符前面带有反斜杠的字符串。 |
| 3. | bin2hex() | 将一串 ASCII 字符转换成十六进制值。 |
| 4. | chop() | rtrim()的别名 |
| 5. | chr() | 从指定的 ASCII 值返回一个字符。 |
| 6. | chunk_split() | 将一串分成一系列更小的部分。 |
| 7. | convert_cyr_string() | 将一个字符串从一种西里尔字符集转换成另一种。 |
| 8. | convert_uudecode() | 解码一个 uuencoded 字符串。 |
| 9. | convert_uuencode() | 使用 uuencode 算法编码字符串。 |
| 10. | count_chars() | 返回一个 ASCII 字符在一个字符串中出现的次数并返回信息。 |
| 11. | crc32() | 计算字符串的 32 位 CRC。 |
| 12. | 地穴() | 单向字符串加密(哈希) |
| 13. | echo() | 输出字符串 |
| 14. | 爆炸() | 将一个字符串分解成一个数组。 |
| 15. | fprintf() | 将格式化字符串写入指定的输出流。 |
| 16. | get _ html _ translation _ table() | 返回 htmlspecialchars()和 htmlentities() 使用的转换表 |
| 17. | 希伯来语() | 将希伯来文本转换为可视文本。 |
| 18. | hebrevc() | 将希伯来文本转换为可视文本，并将新行(\n)转换为< br/ > |
| 19. | html_entity_decode() | 将 HTML 实体转换为字符。 |
| 20. |  | 将字符转换成 HTML 实体。 |
| 21. | html special chars _ decode() | 将一些预定义的 HTML 实体转换成字符。 |
| 22. | htmlspecialchars() | 将一些预定义的字符转换成 HTML 实体。 |
| 23. | 内爆() | 从一个数组的元素中返回一个字符串。 |
| 24. | join() | 内爆的别名() |
| 25. | levenshtein() | 返回两个字符串之间的 Levenshtein 距离。 |
| 26. | localeconv() | 返回区域数字和货币格式信息。 |
| 27. | ltrim() | 从字符串的左边去除空白。 |
| 28. | md5() | 计算字符串的 md5 哈希。 |
| 29. | md5_file() | 计算文件的 md5 哈希。 |
| 30. | 变音() | 计算字符串的变音键。 |
| 31. | money_format() | 返回一个格式化为货币字符串的字符串。 |
| 32. | nl_langinfo() | 返回特定的本地信息。 |
| 33. | nl2br() | 在字符串中的每个换行符前插入 HTML 换行符。 |
| 34. | 数字 _ 格式() | 将一个数字格式化为成组的千位。 |
| 35. | ord() | 返回字符串第一个字符的 ASCII 值。 |
| 36. | parse_str() | 将查询字符串解析成变量。 |
| 37. | print() | 输出字符串。 |
| 38. | printf() | 输出格式化字符串。 |
| 39. | quoted _ printable _ decode() | 解码带引号的可打印字符串。 |
| 40. | quotemeta() | 引用元字符。 |
| 41. | rtrim() | 去除字符串右侧的空白。 |
| 42. | setlocale() | 设置语言环境信息。 |
| 43. | sha1() | 计算字符串的 SHA-1 哈希。 |
| 44. | sha1_file() | 计算文件的 SHA-1 哈希。 |
| 45. | 相似 _ 文本() | 计算两个字符串之间的相似度。 |
| 46. | soundex() | 计算字符串的 soundex 键 |
| 47. | 短跑()T1 | 将格式化字符串写入变量。 |
| 48. | sscanf() | 根据格式从字符串中解析输入。 |
| 49. | str_ireplace() | 替换字符串中的某些字符(不区分大小写) |
| 50. | str_pad() | 将字符串填充到新的长度。 |
| 51. | str_repeat() | 将一个字符串重复指定的次数。 |
| 52. | str_replace() | 替换字符串中的某些字符(区分大小写) |
| 53. | str_rot13() | 对字符串执行 ROT13 编码。 |
| 54. | str_shuffle() | 随机打乱字符串中的所有字符。 |
| 55. | str_split() | 将一个字符串拆分成一个数组。 |
| 56. | str_word_count() | 计算一个字符串中的单词数。 |
| 57. | strcasecmp() | 比较两个字符串(不区分大小写) |
| 58. | strchr() | 查找一个字符串在另一个字符串中的第一次出现(strstr()的别名) |
| 59. | strcmp() | 比较两个字符串(区分大小写) |
| 60. | strcoll() | 基于区域设置的字符串比较 |
| 61. | strcspn() | 返回在找到某些指定字符的任何部分之前，在字符串中找到的字符数。 |
| 62. | strip_tags() | 从字符串中去除 HTML 和 PHP 标签。 |
| 63. | stripcslashs() | 用 addcslashes() 取消对字符串的引用 |
| 64. | 条纹斜线() | 用 addslashes()取消对字符串的引用 |
| 65. | stripos() | 返回一个字符串在另一个字符串中第一次出现的位置(不区分大小写) |
| 66. | strings() | 查找一个字符串在另一个字符串中的第一个匹配项(不区分大小写) |
| 67. | strlen() | 返回字符串的长度 |
| 68. | strnatcasecmp() | 比较两个字符串 |
| 69. | strnatcmp() | 比较两个字符串 |
| 70. | strncacecmp() | 前 n 个字符的字符串比较(不区分大小写) |
| 71. | strncmp() | 前 n 个字符的字符串比较(区分大小写) |
| 72. | strpbrk() | 在字符串中搜索一组字符中的任何一个。 |
| 73. | strpos() | 返回一个字符串在另一个字符串中第一次出现的位置(区分大小写) |
| 74. | strrchr() | 查找一个字符串在另一个字符串中的最后一个匹配项。 |
| 75. | strrev() | 反转一个字符串 |
| 76. | strripos() | 查找一个字符串在另一个字符串中最后一次出现的位置(不区分大小写) |
| 77. | strrpos() | 查找一个字符串在另一个字符串中最后一次出现的位置(区分大小写) |
| 78. | strspn() | 返回在只包含指定字符列表中的字符的字符串中找到的字符数。 |
| 79. | strstr() | 查找一个字符串在另一个字符串中的第一个匹配项(区分大小写) |
| 78. | strtok() | 将一个字符串拆分成更小的字符串。 |
| 79. | strtolow() | 将字符串转换成小写字母。 |
| 80. | 推动器() | 将字符串转换成大写字母。 |
| 81. | strtr() | 翻译字符串中的某些字符。 |
| 82. | substr() | 返回字符串的一部分。 |
| 83. | substr_compare() | 从指定的起始位置比较两个字符串(二进制安全，并可选择区分大小写) |
| 84. | substr_count() | 统计子字符串在字符串中出现的次数。 |
| 85. | substr_replace() | 用另一个字符串替换一个字符串的一部分。 |
| 86. | trim() | 去除字符串两边的空白。 |
| 87. | ucfirst() | 将字符串的第一个字符转换为大写。 |
| 88. | ucwords() | 将字符串中每个单词的第一个字符转换为大写。 |
| 89. | vfprintf() | 将格式化字符串写入指定的输出流。 |
| 90. | vprintf() | 输出格式化字符串。 |
| 91. | vsprintf() | 将格式化字符串写入变量。 |
| 92. | wordwrap() | 将字符串换行到给定的字符数。 |

### **字符串常量**

| 1. | CRYPT_SALT_LENGTH | 包含系统默认加密方法的长度。对于标准 DES 加密，长度为 2 |
| 2. | CRYPT_STD_DES | 如果支持基于标准 DES 的 2 字符 salt 加密，则设置为 1，否则设置为 0 |
| 3. | CRYPT_EXT_DES | 如果支持 9 字符 salt 的扩展 DES 加密，则设置为 1，否则设置为 0 |
| 4. | CRYPT_MD5 | 如果支持以＄1＄开始的 12 字符 salt 的 MD5 加密，则设置为 1，否则设置为 0 |
| 5. | 地穴 _ 河豚 | 如果支持以$2$或$2a$开始的 16 字符 salt 的 Blowfish 加密，则设置为 1，否则为 0 |
| 6. | html _ specialchars | 将一些预定义的字符转换成 HTML 实体。 |
| 7. | HTML_ENTITIES | 将输入字符串中的特殊字符转换成 HTML 字符的形式。 |
| 8. | ent _ compat | 转换双引号 |
| 9. | ENT _ 引号 | 将转换单引号和双引号。 |
| 10. | ent _ no quotes | 将使单引号和双引号不被转换。 |
| 11. | ENT_IGNORE | 静默丢弃无效的代码单元序列，而不是返回空字符串。不建议使用此标志，因为它可能有安全隐患。 |
| 12. | ENT_SUBSTITUTE | 用 Unicode 替换字符 U+FFFD (UTF-8)或&# xFFFD；替换无效的代码单元序列；(否则)而不是返回空字符串。 |
| 13. | ENT_DISALLOWED | 用 Unicode 替换字符 U+FFFD (UTF-8)或&# xFFFD；替换给定文档类型的无效代码点；(否则)而不是让它们保持原样。例如，这可能有助于确保嵌入外部内容的 XML 文档的格式良好。 |
| 14. | ENT_HTML401 | 处理代码为 HTML 4.01。 |
| 15. | ENT_XML1 | 将代码作为 XML 1 处理。 |
| 16. | ENT_XHTML | 将代码作为 XHTML 处理。 |
| 17. | ENT_HTML5 | 把代码当做 HTML 5 来处理。 |
| 18. | CHAR_MAX | 如果一个数组元素等于 CHAR_MAX，则不再分组。 |
| 19. | LC_CTYPE | 进行字符分类和转换。 |
| 20. | LC_NUMERIC | 用于小数分隔符。 |
| 21. | LC_TIME | 用于日期和时间格式化。 |
| 22. | LC_COLLATE | 用于字符串比较。 |
| 23. | 信用证 _ 货币 | 表示 localeconv() |
| 24. | LC_ALL | 对于所有 LC_ functions。 |
| 25. | LC_MESSAGES | 为系统响应。 |
| 26. | STR_PAD_LEFT | 填充输入字符串的左侧。 |
| 27. | STR_PAD_RIGHT | 填充输入字符串的右侧。 |
| 28. | STR_PAD_BOTH | 填充输入字符串的两边。 |

### **数学函数**

数学函数用于处理整数和浮点类型范围内的值。

| 1. | abs() | 返回一个数的绝对值。 |
| 2. | acos() | 返回一个数字的反余弦值。 |
| 3. | acosh() | 返回一个数字的反双曲余弦值。 |
| 4. | 阿辛() | 返回一个数字的反正弦值。 |
| 5. | 就为了使用一个同样的描述法 | 返回一个数字的反双曲正弦值。 |
| 6. | 阿坦() | 返回一个介于-pi/2 和+pi/2 弧度之间的反正切值。 |
| 7. | atan2() | 以介于-pi 和+pi 弧度之间的数值形式返回(x，y)点的角度θ。 |
| 8. | 阿坦赫() | 返回一个数字的反双曲正切值。 |
| 9. | base_convert() | 将数字从一种基数转换成另一种基数。 |
| 10. | bindec() | 将二进制数转换成十进制数。 |
| 11. | ceil() | 返回向上舍入到最接近的整数的数值。 |
| 12. | cos() | 返回一个数字的余弦值。 |
| 13. | cosh() | 返回一个数字的双曲余弦值。 |
| 14. | decbin() | 将十进制数转换为二进制数。 |
| 15. | 十六烷() | 将十进制数转换为十六进制数。 |
| 16. | 煎() | 将十进制数转换为八进制数。 |
| 17. | deg2rad() | 将度数转换成弧度数。 |
| 18. | exp() | 返回 E 的值 |
| 19. | expm1() | 返回 E 的值 |
| 20. | 楼层() | 返回向下舍入到最接近的整数的数值。 |
| 21. | fmod() | 返回参数除法的余数(模)。 |
| 22. | getrandmax() | 返回调用 rand()函数所能返回的最大随机数。 |
| 23. | hexdec() | 将十六进制数转换为十进制数。 |
| 24. | 海波() | 返回直角三角形斜边的长度。 |
| 25. | is_finite() | 如果值是一个有限的数字，则返回 true。 |
| 26. | is_infinite() | 如果一个值是无穷大，则返回 true。 |
| 27. | is_nan() | 如果值不是数字则返回 true |
| 28. | lcg_value() | 返回(0，1) 范围内的伪随机数 |
| 29. | log() | 返回一个数的自然对数(以 E 为底)。 |
| 30. | log10() | 返回一个数以 10 为底的对数。 |
| 31. | log1p() | 返回日志(1+数字) |
| 32. | max() | 返回两个指定数字中最大值的数字。 |
| 33. | min() | 返回两个指定数字中最小值的数字。 |
| 34. | mt_getrandmax() | 返回 mt_rand() 能够返回的最大可能值 |
| 35. | mt_rand() | 使用 Mersenne Twister 算法返回随机整数。 |
| 36. | mt_srand() | 播种梅森图随机数生成器。 |
| 37. | octdec() | 将八进制数转换成十进制数。 |
| 38. | pi() | 返回圆周率的值 |
| 39. | pow() | 返回 x 的 y 次方值。 |
| 40. | rad2deg() | 将弧度数转换成度数 |
| 41. | 兰德() | 返回一个随机整数 |
| 42. | 回合() | 将一个数字舍入到最接近的整数。 |
| 43. | sin() | 返回一个数字的正弦值。 |
| 44. | sinh() | 返回一个数字的双曲正弦值。 |
| 45. | sqrt() | 返回一个数字的 sqrt。 |
| 46. | srand() | 种子随机数生成器。 |
| 47. | 谭() | 返回一个角度的正切值。 |
| 48. | tanh() | 返回一个角度的双曲正切值。 |

### **数学常数**

| 1. | M_E | 返回 e(近似值。2.718) |
| 2. | M _ 欧拉 | 返回欧拉常数(近似值)。0.577) |
| 3. | M_LNPI | 返回圆周率的自然对数(近似值)。1.144) |
| 4. | M_LN2 | 返回 2 的自然对数(近似值)。0.693) |
| 5. | M_LN10 | 返回 10 的自然对数(近似值)。2.302) |
| 6. | M_LOG2E | 返回 E 的以 2 为底的对数(近似值)。1.442) |
| 7. | M_LOG10E | 返回 E 的以 10 为底的对数(近似值)。0.434) |
| 8. | M_PI | 返回圆周率(近似值。3.14159) |
| 9. | M_PI_2 | 返回 PI/2(近似值。1.570) |
| 10. | M_PI_4 | 返回π/4(近似值。0.785) |
| 11. | M_1_PI | 返回 1/PI(近似值。0.318) |
| 12. | M_2_PI | 返回 2/PI(近似值。0.636) |
| 13. | M_SQRTPI | 返回圆周率的平方根(近似值)。1.772) |
| 14. | M_2_SQRTPI | 返回 2/圆周率的平方根(近似值。1.128) |
| 15. | M_SQRT1_2 | 返回 1/2 的平方根(近似值)。0.707) |
| 16. | M_SQRT2 | 返回 2 的平方根(近似值)。1.414) |
| 18 | M_SQRT3 | 返回 3 的平方根(近似值)。1.732) |

### **日期/时间功能**

日期/时间函数允许从运行 PHP 脚本的服务器获取日期和时间。这些函数也可用于根据需要设置日期/时间函数的格式。

| 1. | 检查日期() | 验证公历数据 |
| 2. | 日期 _ 默认 _ 时区 _ 获取() | 返回默认时区。 |
| 3. | 日期默认时区设置() | 设置默认时区。 |
| 4. | date_sunrise() | 返回时间或地点的日出时间。 |
| 5. | date_sunset() | 返回时间或地点的日落时间。 |
| 6. | 日期() | 格式化本地时间/日期。 |
| 7. | getdate() | 返回包含 Unix 时间戳的日期和时间戳信息的数组。 |
| 8. | gettimeofday() | 返回包含当前时间信息的数组。 |
| 9. | gmdate() | 格式化 GMT/UTC 日期/时间 |
| 10. | gmmktime() | 返回 GMT 表的 Unix 时间戳。 |
| 11. | gmstrftime() | 根据区域设置格式化 GMT/UTC 时间/日期。 |
| 12. | idate() | 将本地时间/日期格式化为整数。 |
| 13. | 本地时间() | 返回一个包含 Unix 时间戳的时间部分的数组。 |
| 14. | 微时间() | 以微秒为单位返回当前时间。 |
| 15. | mktime() | 返回日期的 Unix 时间戳。 |
| 16. | strftime() | 根据区域设置格式化本地时间日期。 |
| 17. | strptime() | 解析 strftime()生成的时间/日期 |
| 18. | strtotime() | 将英文文本日期或时间解析成 Unix 时间戳。 |
| 19 | 时间() | 以 Unix 时间戳的形式返回当前时间。 |

### **日期/时间常数**

| 1. | 日期 _ 原子 | 原子(例:2005-08-15T16:13:03+0000) |
| 2. | 日期 _ 饼干 | HTTP cookie(例如:世界协调时 2005 年 8 月 14 日 16:13:03 日星期日) |
| 3. | 日期 _ISO8601 | ISO-8601(例如:2005-08-14T16:13:03+0000) |
| 4. | date _ RFC 822 | RFC 822(例如:世界协调时 2005 年 8 月 14 日 16 时 13 分 03 秒) |
| 5. | date _ RFC 850 | RFC 850(例如:世界协调时 2005 年 8 月 14 日星期日 16:13:03) |
| 6. | date _ RFC 1036 | RFC 1036(例如:世界协调时 2005 年 8 月 14 日星期日 16:13:03) |
| 7. | date _ RFC 1123 | RFC 1123(例如:世界协调时 2005 年 8 月 14 日 16 时 13 分 03 秒) |
| 8. | date _ RFC 2822 | RFC 2822(星期日，2005 年 8 月 14 日 16:13:03 +0000) |
| 9. | date _ RSS | 【国际标准时间 2005 年 8 月 14 日星期日 16 时 13 分 03 秒】 |
| 10. | 日期 _W3C | 万维网联盟(举例:2005-08-14T16:13:03+0000) |

### **日历功能**

日历扩展包含简化两种不同日历格式之间转换的功能。

| 1. | 月份天数() | 返回指定年份和日历中一个月的天数 |
| 2. | cal_from_jd() | 将儒略日计数转换为指定日历的日期。 |
| 3. | cal_info() | 返回给定日历的信息 |
| 4. | cal_to_jd() | 将日期转换为儒略日计数。 |
| 5. | 复活节 _ 日期() | 返回指定月份复活节午夜的 Unix 时间戳。 |
| 6. | 复活节 _ 日() | 返回指定年份的复活节在 3 月 21 日之后的天数。 |
| 7. | frechdooj() | 将法国共和日转换为儒略日计数。 |
| 8. | GregorianToJD() | 将公历日期转换为儒略日计数。 |
| 9. | JDDayOfWeek() | 返回星期几。 |
| 10. | JDMonthName() | 返回月份名称。 |
| 11. | JDToFrench() | 将儒略日计数转换为法国共和日。 |
| 12. | JDToGregorian() | 将儒略日计数转换为公历日期。 |
| 13. | 犹太人() | 将儒略日计数转换为犹太日期。 |
| 14. | JDToJulian() | 将儒略日计数转换为儒略日。 |
| 15. | jdtounix() | 将儒略日计数转换为 Unix 时间戳。 |
| 16. | 犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人犹太人 | 将犹太日期转换为儒略日计数。 |
| 17. | JulianToJD() | 将儒略日转换成儒略日计数。 |
| 18. | unixtojd() | 将 Unix 时间戳转换为儒略日计数。 |

### **日历常数**

| 1. | CAL_GREGORIAN | 公历 |
| 2. | CAL_JULIAN | 儒略历 |
| 3. | CAL_JEWISH | 犹太历 |
| 4. | CAL_FRENCH | 法国共和历。 |
| 5. | 校准数量 | 可用日历的数量。 |
| 6. | CAL_DOW_DAYNO | 整数表示一周中的某一天，其中 0 表示星期日，6 表示星期六。 |
| 7. | CAL_DOW_SHORT | 一周中某一天的英文缩写名称。 |
| 8. | CAL_DOW_LONG | 一周中某一天的英文名称。 |
| 9. | CAL _ MONTH _ GREGORIAN _ SHORT | 缩写的公历月份名称。 |
| 10. | CAL_MONTH_GREGORIAN_LONG | 公历月份名称。 |
| 11. | CAL_MONTH_JULIAN_SHORT | 缩写的儒略月名。 |
| 12. | CAL_MONTH_JULIAN_LONG | 儒略月的名字。 |
| 13. | CAL_MONTH_JEWISH | 犹太月名。 |
| 14. | CAL_MONTH_FRENCH | 法国共和月名称。 |
| 15. | CAL_EASTER_DEFAULT | 根据儒略历计算 1753 年以前的复活节，根据公历计算以后的复活节。 |
| 16. | CAL_EASTER_ROMAN | 根据儒略历计算 1583 年以前的复活节，根据公历计算以后的复活节。 |
| 17. | CAL _ EASTER _ ALWAYS _ GREGORIAN | 根据公历计算复活节。 |
| 18. | 卡尔 _ 复活节 _ 总是 _ 朱利安 | 根据儒略历计算复活节。 |
| 19. | CAL _ JEWISH _ ADD _ ALAFIM _ GERESH | 添加一个 geresh 符号(类似单引号)作为年份数字的千位分隔符。 |
| 20. | CAL_JEWISH_ADD_ALAFIM | 将单词 alafim 作为千位分隔符添加到年份数字中。 |
| 21. | CAL _ JEWISH _ ADD _ GERESHAYIM | 在日期和年份数字的最后一个字母前添加一个 gershayim 符号(类似于双引号)。 |

### **目录功能**

目录功能用于检索目录及其内容的相关信息。

| 1. | chdir() | 改变当前目录 |
| 2. | chroot() | 改变当前进程的根目录。 |
| 3. | dir() | 打开目录句柄并返回一个对象。 |
| 4. | closedir() | 关闭目录句柄。 |
| 5. | 已绘制() | 返回当前目录。 |
| 6. | opendir() | 打开一个目录句柄。 |
| 7. | readdir() | 从目录句柄返回一个条目。 |
| 8. | rewinddir() | 重置一个目录句柄。 |
| 9. | 扫描() | 列出指定路径下的文件和目录。 |

### **目录常数**

| 1. | 目录 _ 分隔符 | 不同的操作系统有不同的目录分隔符。在 Windows 中是\在 Linux 中是/。DIRECTORY_SEPARATOR 对于操作系统目录分隔符是常量。 |
| 2. | 路径 _ 分隔符 | windows 上分号，否则冒号。 |

### **文件系统功能**

这些函数允许访问和操作文件系统。

| 1. | 基本名称() | 返回路径的文件名部分。 |
| 2. | chgrp() | 改变文件组。 |
| 3. | chmod() | 改变文件模式 |
| 4. | chown() | 改变文件所有者 |
| 5. | clearstatcache() | 清除文件状态缓存 |
| 6. | 复制() | 复制一个文件 |
| 7. | 删除() | 删除一个文件 |
| 8. | dirname() | 返回路径的目录名部分 |
| 9. | 磁盘可用空间()&#124;磁盘可用空间() | 返回一个目录的空闲空间 |
| 10. | 磁盘总空间() | 返回一个目录的总大小 |
| 11. | fclose() | 关闭打开的文件 |
| 12. | feof() | 测试打开文件的文件尾 |
| 13. | fflush() | 将缓冲输出刷新到打开的文件。 |
| 14. | fgetc() | 从打开的文件中返回一个字符 |
| 15. | fgetcsv() | 检查并解析一个打开文件中的一行。 |
| 16. | fgets() | 从打开的文件中返回一行。 |
| 17. | FGS() | 从打开的文件中返回一行，去掉 HTML 和 PHP 标签。 |
| 18. | file() | 将文件读入数组 |
| 19. | file_exists() | 检查文件或目录是否存在。 |
| 20. | 文件 _ 获取 _ 内容() | 将文件读入字符串 |
| 21. | 文件 _ 上传 _ 内容 | 将字符串写入文件 |
| 22. | fileatime() | 返回文件的最后访问时间 |
| 23. | filectime() | 返回文件的最后更改时间。 |
| 24. | 文件组() | 返回文件的组 ID |
| 25. | fileinode() | 返回文件的索引节点号 |
| 26. | filemtime() | 返回文件的最后修改时间 |
| 27. | 文件所有者() | 返回文件的用户 ID(所有者) |
| 28. | fileperms() | 返回文件的权限。 |
| 29. | filesize() | 返回文件大小。 |
| 30. | 螺纹类型() | 返回文件类型。 |
| 31. | flock() | 锁定或释放文件。 |
| 32. | fnmatch() | 根据指定模式匹配文件名或字符串 |
| 33. | fopen() | 打开文件或网址 |
| 34. | fpassthru() | 从打开的文件中读取，直到 EOF，并将结果写入输出缓冲区。 |
| 35. | fputcsv() | 将一行格式化为 CSV 格式，并将其写入一个打开的文件。 |
| 36. | fputs() | fwrite 的别名。 |
| 37. | fread() | 从打开的文件中读取。 |
| 38. | fscanf() | 根据指定的格式从打开的文件中解析输入。 |
| 39. | fseek() | 在打开的文件中查找。 |
| 40. | fstat() | 返回关于打开文件的信息。 |
| 41. | ftell() | 返回打开文件的当前位置。 |
| 42. | ftruncate() | 将打开的文件截断到指定长度。 |
| 43. | fwrite() | 写入一个打开的文件。 |
| 44. | glob() | 返回与指定模式匹配的文件名/目录数组。 |
| 45. | is_dir() | 检查一个文件是否是一个目录。 |
| 46. | is_executable() | 检查文件是否可执行。 |
| 47. | is_file() | 检查文件是否为常规文件。 |
| 48. | is_link() | 检查文件是否是链接。 |
| 49. | is_readable() | 检查文件是否可读。 |
| 50. | is_uploaded_file() | 检查文件是否通过 HTTP POST 上传 |
| 51. | is _ writable()&#124; is _ writeable() | 检查文件是否可读。 |
| 52. | link() | 创建一个硬链接 |
| 53. | 链接信息() | 返回关于硬链接的信息。 |
| 54. | 【T0 状态(): | 返回关于文件或符号链接的信息 |
| 55. | mkdir() | 创建一个目录。 |
| 56. | move_uploaded_file() | 将上传的文件移动到新位置。 |
| 57. | parse_ini_file() | 解析配置文件。 |
| 58. | pathinfo() | 返回关于文件路径的信息。 |
| 59. | pclose() | 关闭由 popen() 打开的管道 |
| 60. | popen() | 打开管道 |
| 61. | readfile() | 读取文件并将其写入输出缓冲区。 |
| 62. | 读取链接() | 返回一个符号链接的目标。 |
| 63. | realpath() | 返回绝对路径名。 |
| 64. | 重命名() | 重命名文件或目录。 |
| 65. | 倒带() | 倒回一个文件指针。 |
| 66. | 是指() | 删除空目录。 |
| 67. | set_file_buffer() | 设置打开文件时的缓冲区大小。 |
| 68. | stat() | 返回关于文件的信息。 |
| 69. | 符号链接() | 创建一个符号链接 |
| 70. | tempnam() &#124; tmpfile() | 创建一个唯一的临时文件 |
| 71. | 触摸() | 设置文件的访问和修改时间。 |
| 72. | umask() | 更改文件的文件权限。 |
| 73. | unlink() | 删除文件。 |

### **文件系统常数**

| 1. | GLOB_BRACE | 扩展以匹配‘a’、‘b’或‘c’ |
| 2. | GLO _ onlydir | 仅返回与模式匹配的目录条目 |
| 3. | 全球标记 | 给每个返回的目录添加一个斜杠 |
| 4. | 全球无排序 | 按照文件在目录中出现的样子返回文件(不排序)。不使用该标志时，路径名按字母顺序排序 |
| 5. | 全球皆然 | 如果没有找到匹配的文件，返回搜索模式 |
| 6. | 全球景观 | 反斜杠不引用元字符。 |
| 7. | 全球错误 | 在读取错误时停止(如不可读的目录)，默认情况下错误被忽略。 |
| 8. | 路径信息目录名 | 返回关于路径目录的信息。 |
| 9. | 路径信息基本名称 | 返回关于路径基本名的信息。 |
| 10. | PATHINFO_EXTENSION | 返回关于路径扩展的信息。 |
| 11. | 文件使用包含路径 | 在包含路径中搜索文件。 |
| 12. | 文件 _ 追加 | 将文件追加到文件中。为此，目标文件需要是可写的。 |
| 13. | 文件 _ 忽略 _ 新 _ 行 | 省略每个数组元素末尾的换行符。 |
| 14. | FILE_SKIP_EMPTY_LINES | 跳过空行。 |

### **压缩功能**

这些功能允许你阅读 zip 文件。zip 扩展需要 libzip，这是一个 C 库，用于读取、创建和修改 ZIP 存档。

| 1. | zip_close() | 关闭一个 ZIP 文件 |
| 2. | zip_entry_close() | 关闭 ZIP 文件中的一个条目 |
| 3. | zip _ entry _ compressed size() | 返回 ZIP 文件中条目的压缩大小。 |
| 4. | zip _ entry _ compress method() | 返回 ZIP 文件中条目的压缩方法。 |
| 5. | zip_entry_filesize() | 返回 ZIP 文件中条目的实际文件大小。 |
| 6. | zip_entry_name() | 返回 ZIP 文件中条目的名称。 |
| 7. | zip_entry_open() | 打开 ZIP 文件中的条目进行读取。 |
| 8. | zip_entry_read() | 读取 ZIP 文件中打开的条目。 |
| 9. | zip_open() | 打开一个 ZIP 文件 |
| 10. | zip_read() | 读取 ZIP 文件中的下一个条目。 |

### **过滤功能**

这些函数用于验证和过滤来自不安全输入源的数据。默认情况下，这些过滤功能处于启用状态。

| 1. | filter_has_var() | 检查指定输入类型的变量是否存在。 |
| 2. | filter_id() | 返回指定过滤器的 ID 号。 |
| 3. | filter_input() | 从脚本外部获取输入并过滤。 |
| 4. | 过滤器 _ 输入 _ 数组() | 从脚本外部获取多个输入并过滤它们。 |
| 5. | filter_list() | 返回所有支持的过滤器的数组 |
| 6. | filter_var_array() | 获取多个变量并过滤。 |
| 7. | filter_var() | 获取一个变量并过滤它。 |

### **过滤常数**

| 1. | 过滤 _ 默认 | 什么都不做，随意剥离/编码特殊字符。相当于 FILTER_UNSAFE_RAW |
| 2. | FILTER_FLAG_NONE | 允许无标志 |
| 3. | FILTER_FLAG_ALLOW_OCTAL | 仅适用于以零(0)开始的八进制数字输入。这仅允许后续数字为 0-7 |
| 4. | FILTER_FLAG_ALLOW_HEX | 仅适用于以 0x/0X 作为十六进制数开头的输入。这只允许后续字符为 a-fA-F0-9 |
| 5. | FILTER_FLAG_STRIP_LOW | 剥离 ASCII 值低于 32 的字符 |
| 6. | FILTER_FLAG_STRIP_HIGH | 剥离 ASCII 值大于 127 的字符 |
| 7. | FILTER_FLAG_ENCODE_LOW | 对 ASCII 值小于 32 的字符进行编码 |
| 8. | FILTER_FLAG_ENCODE_HIGH | 对 ASCII 值大于 127 的字符进行编码 |
| 9. | FILTER_FLAG_ENCODE_AMP | 编码& |
| 10. | FILTER _ FLAG _ NO _ ENCODE _ QUOTES | 不编码’和“ |
| 11. | FILTER _ FLAG _ EMPTY _ STRING _ NULL | 未使用 |
| 12. | 过滤 _ 标志 _ 允许 _ 分数 | 允许句号(。)作为数字中的分数分隔符 |
| 13. | 过滤 _ 标志 _ 允许 _ 千位 | 允许逗号(，)作为数字中的千位分隔符 |
| 14. | 过滤器 _ 标志 _ 允许 _ 科学 | 允许在数字中用 E 或 E 表示科学记数法 |
| 15. | 过滤器 _ 标志 _ 路径 _ 要求 | URL 必须包含路径部分 |
| 16. | FILTER _ FLAG _ QUERY _ REQUIRED | URL 必须包含一个查询字符串 |
| 17. | 过滤器 _ 标志 _IPV4 | 允许 IP 地址采用 IPv4 格式 |
| 18. | 过滤器 _ 标志 _IPV6 | 允许 IP 地址采用 IPv6 格式 |
| 19. | FILTER_FLAG_NO_RES_RANGE | 无法验证保留的 IPv4 范围:0.0.0.0/8、169.254.0.0/16、127.0.0.0/8 和 240.0.0.0/4，以及保留的 IPv6 范围:::1/128，:/128，::ffff:0:0/96 和 fe80::/10 |
| 20. | FILTER _ FLAG _ NO _ PRIV _ RANGE | 无法验证专用 IPv4 范围:10.0.0.0/8、172.16.0.0/12 和 192.168.0.0/16，以及以 FD 或 FC 开头的 IPv6 地址 |
| 21. | FILTER _ FLAG _ EMAIL _ UNICODE | 允许电子邮件地址的本地部分包含 Unicode 字符 |
| 22. | FILTER_REQUIRE_SCALAR | 该值必须是标量 |
| 23. | FILTER_REQUIRE_ARRAY | 该值必须是一个数组 |
| 24. | 过滤器 _ 力 _ 阵列 | 将标量值视为一个数组，标量值是唯一的元素 |
| 25. | 过滤无效开启失败 | 对于无法识别的布尔值，失败时返回空值 |
| 26. | 过滤 _ 验证 _ 布尔 | 验证一个布尔值 |
| 27. | 过滤 _ 验证 _ 电子邮件 | 将值验证为有效的电子邮件地址 |
| 28. | FILTER_VALIDATE_FLOAT | 验证浮点值 |
| 29. | FILTER_VALIDATE_INT | 将值验证为整数 |
| 30. | FILTER_VALIDATE_IP | 将值验证为 IP 地址 |
| 31. | FILTER_VALIDATE_MAC | 将值验证为 MAC 地址 |
| 32. | FILTER_VALIDATE_REGEXP | 根据正则表达式验证值 |
| 33. | 过滤 _ 验证 _ 网址 | 将值验证为 URL |
| 34. | FILTER_SANITIZE_EMAIL | 删除电子邮件地址中的所有非法字符 |
| 35. | 过滤 _ 消毒 _ 编码 | 删除/编码特殊字符 |
| 36. | FILTER _ SANITIZE _ MAGIC _ 引号 | 应用 addslashes() |
| 37. | 过滤器 _ 消毒 _ 数量 _ 浮动 | 删除所有字符，除了数字、+-号和可选的。，eE |
| 38. | FILTER _ SANITIZE _ NUMBER _ INT | 删除除数字和+ -符号之外的所有字符 |
| 39. | FILTER _ SANITIZE _ SPECIAL _ CHARS | 删除特殊字符 |
| 40. | FILTER_SANITIZE_STRING | 从字符串中删除标签/特殊字符 |
| 41. | FILTER_SANITIZE_STRIPPED | 过滤器 _ 消毒 _ 字符串的别名 |
| 42. | FILTER_SANITIZE_URL | 从 s URL 中删除所有非法字符 |
| 43. | FILTER_UNSAFE_RAW | 什么都不做，随意剥离/编码特殊字符 |
| 44. | FILTER_CALLBACK | 调用自定义函数过滤数据 |
| 45. | 输入 _ 发布 | 发布变量 |
| 46. | 输入 _ 获取 | 获取变量 |
| 47. | 输入 _COOKIE | COOKIE 变量 |
| 48. | 输入 _ 环境 | 环境变量 |
| 49. | 输入 _ 服务器 | 服务器变量 |

### **邮件功能**

邮件功能允许直接从脚本发送邮件。

| 1. | ezmlm_hash() | 通过 EZMLM 邮件列表系统计算哈希值。 |
| 2. | 邮件() | 允许您直接从脚本发送电子邮件。 |

### **FTP 功能**

FTP 功能让客户端通过文件传输协议(FTP)访问文件服务器。FTP 功能用于打开、登录和关闭连接、上传、下载、重命名、删除和从文件服务器获取文件信息。

| 1. | ftp_alloc() | 为上传到 FTP 服务器的文件分配空间。 |
| 2. | ftp_cdup() | 将当前目录更改为 FTP 服务器上的父目录。 |
| 3. | ftp_chdir() | 改变 FTP 服务器上的当前目录 |
| 4. | ftp_chmod() | 通过 FTP 设置文件权限 |
| 5. | ftp_close() | 关闭 FTP 连接。 |
| 6. | ftp_connect() | 打开一个 FTP 连接 |
| 7. | ftp_delete() | 删除 FTP 服务器上的文件。 |
| 8. | ftp_exec() | 在 FTP 服务器上执行程序/命令。 |
| 9. | FTP _ fgt() | 从 FTP 服务器下载文件并保存到打开的文件中。 |
| 10. | ftp_fput() | 从打开的文件上传并保存到 FTP 服务器上的文件中。 |
| 11. | ftp_get_option() | 返回 FTP 连接的运行时行为。 |
| 12. | ftp_get() | 从 FTP 服务器下载文件。 |
| 13. | ftp_login() | 登录到 FTP 连接 |
| 14. | ftp_mdtm() | 返回指定文件的最后修改时间。 |
| 15. | ftp_mkdir() | 在 FTP 服务器上创建新目录。 |
| 16. | ftp_nb_continue() | 继续检索/发送文件(非阻塞) |
| 17. | ftp_nb_fget() | 从 FTP 服务器下载文件并保存到打开的文件中(非阻塞) |
| 18. | ftp_nb_fput() | 从打开的文件上传并保存到 FTP 服务器上的文件(非阻塞) |
| 19. | ftp_nb_get() | 从 FTP 服务器下载文件(非阻塞) |
| 20. | ftp_nb_put() | 上传文件到 FTP 服务器(非阻塞) |
| 21. | ftp_nlist() | 列出 FTP 服务器上指定目录下的文件。 |
| 22. | ftp_pasv() | 打开或关闭被动模式。 |
| 23. | ftp_put() | 上传文件到 FTP 服务器。 |
| 24. | ftp_pwd() | 返回当前目录名。 |
| 25. | ftp_quit() | FTP _ close()的别名 |
| 26. | ftp_raw() | 向 FTP 服务器发送原始命令 |
| 27. | ftp_rawlist() | 返回指定目录下文件的详细列表 |
| 28. | ftp_rename() | 重命名 FTP 服务器上的文件或目录。 |
| 29. | ftp_rmdir() | 删除 FTP 服务器上的目录。 |
| 30. | ftp_set_option() | 设置 FTP 连接的运行时选项 |
| 31. | ftp_site() | 向服务器发送站点命令。 |
| 32. | ftp_size() | 返回指定文件的大小。 |
| 33. | ftp_ssl_connect() | 打开安全的 SSL-FTP 连接 |
| 34. | ftp_systype() | 返回 FTP 服务器的系统类型标识符。 |

### **FTP 常量**

| 1. | FTP _ ascii \ FTP _ 文本 | 是 FTP 传输模式。 |
| 2. | FTP_BINARY &#124; FTP_IMAGE | 是 FTP 传输模式。 |
| 3. | FTP_TIMEOUT_SEC | 网络操作超时 |
| 4. | FTP_AUTOSEEK | 设置其他运行时 FTP 选项。 |
| 5. | FTP_AUTORESUME | 自动确定 GET 和 PUT 请求的恢复位置和开始位置。需要启用 FTP_AUTOSEEK。 |
| 6. | FTP_FAILED | 异步传输失败。 |
| 7. | FTP _ 完成 | 异步传输已完成。 |
| 8. | FTP_MOREDATA | 异步传输正在进行中。 |

### **HTTP 功能**

| 1. | header() | 向客户端发送原始 HTTP 报头。 |
| 2. | headers_list() | 返回已发送(或准备发送)的响应头列表 |
| 3. | headers_sent() | 检查 HTTP 报头是否已经发送/发送到哪里。 |
| 4. | setcookie() | 向客户端发送 HTTP cookie。 |
| 5. | setrawcookie() | 发送 HTTP cookie，但不对 cookie 值进行 URL 编码。 |

### **简单的 XML 函数**

允许我们轻松地操作和获取 XML 数据。一旦知道了 XML 文档的结构或布局，它就可以获得元素的名称、属性和文本内容。简单 XML 将 XML 文档转换成可以像数组和对象一样迭代的数据结构。

| 1. | __construct() | 创建一个新的 SimpleXML 元素对象 |
| 2. | addAttribute() | 向 SimpleXML 元素添加一个属性 |
| 3. | addChild() | 从 SimpleXML 元素添加一个子元素。 |
| 4. | asXML() | 从 SimpleXML 元素获取 XML 字符串。 |
| 5. | 属性() | 获取 SimpleXML 元素的属性。 |
| 6. | 儿童() | 获取指定节点的子节点。 |
| 7. | getDocNamespaces() | 获取 XML 文档的名称空间。 |
| 8. | getName() | 获取 SimpleXML 元素的名称。 |
| 9. | getNamespace() | 从 XML 数据中获取名称空间。 |
| 10. | registerXPathNamespace() | 为下一个 XPath 查询创建名称空间上下文。 |
| 11. | 简单 XML _ 导入 _dom() | 从一个 DOM 节点获取一个 SimpleXMLElement 对象。 |
| 12. | simplexml_load_file() | 从 XML 文档中获取一个 SimpleXMLElement 对象。 |
| 13. | 简单 XML _ 加载 _ 字符串() | 从 XML 字符串中获取一个 SimpleXMLElement 对象。 |
| 14. | xpath() | 对 XML 数据运行 XPath 查询。 |

### **LIBXML 函数**

这些函数与 SimpleXML、XSLT 和 DOM 函数一起使用。

| 1. | libxml_clear_errors() | 清除 libxml 错误缓冲区 |
| 2. | libxml_get_errors() | 检索错误数组 |
| 3. | libxml_get_last_error() | 从 libxml 中检索最后一个错误 |
| 4. | libxml _ set _ streams _ context() | 为下一次 libxml 文档装载或写入设置流上下文。 |
| 5. | libxml _ use _ internal _ errors() | 禁用 libxml 错误并允许用户根据需要获取错误信息。 |

### **LIBXML 常量**

| 1. | LIBXML_BIGLINES | 正确报告大于 65535 的行号 |
| 2. | LIBXML_COMPACT | 设置小节点分配优化。这可能会提高应用程序的性能 |
| 3. | LIBXML_DOTTED_VERSION | 获取带点的 libxml 版本(例如 2.6.5 或 2.6.17) |
| 4. | LIBXML_DTDATTR | 设置默认 DTD 属性 |
| 5. | LIBXML_DTDLOAD | 加载外部子集 |
| 6. | LIBXML_DTDVALID | 用 DTD 确认 |
| 7. | LIBXML_ERR_ERROR | 获取可恢复错误 |
| 8. | LIBXML_ERR_FATAL | 出现致命错误 |
| 9. | LIBXML_ERR_NONE | 没有错误 |
| 10. | LIBXML_ERR_WARNING | 获得简单警告 |
| 11. | LIBXML_HTML_NOIMPLIED | 设置 HTML_PARSE_NOIMPLIED 标志。这将关闭自动添加隐含的 html/body 元素 |
| 12. | LIBXML_HTML_NODEFDTD | 设置 HTML_PARSE_NODEFDTD 标志。如果没有找到文档类型，这将阻止添加默认文档类型 |
| 13. | LIBXML_NOBLANKS | 删除空白节点 |
| 14. | LIBXML_NOCDATA | 将 CDATA 设置为文本节点 |
| 15. | libxml _ 命名空间 | 修改空标签(如< br/ >到< br > < /br >)，仅在 DOMDocument- > save()和 DOMDocument- > saveXML()函数中可用 |
| 16. | LIBXML_NOENT | 替代实体 |
| 17. | LIBXML_NOERROR | 不显示错误报告 |
| 18. | LIBXML_NONET | 加载文件时停止网络访问 |
| 19. | LIBXML_NOWARNING | 不显示警告报告 |
| 20. | LIBXML_NOXMLDECL | 保存文档时删除 XML 声明 |
| 21. | LIBXML_NSCLEAN | 删除多余的名称空间声明 |
| 22. | LIBXML_PARSEHUGE | 设置 XML_PARSE_HUGE 标志。这放宽了解析器的任何硬编码限制，比如文档的最大深度或文本节点的大小 |
| 23. | LIBXML_PEDANTIC | 设置 XML_PARSE_PEDANTIC 标志。这使得迂腐的错误报告 |
| 24. | LIBXML_XINCLUDE | 使用 XInclude 替换 |
| 25. | LIBXML_VERSION | 获取 libxml 版本(如 20605 或 20617) |
| 26. | LIBXML_SCHEMA_CREATE | 在 XSD 模式验证期间创建默认或固定值节点 |

### **XML 解析器函数**

XML 是一种旨在用于标准化结构化文档交换的数据格式。它们有助于解析 XML 文档。然而，它们无助于验证文档。XML 解析器函数使我们能够创建 XML 解析器并为 XML 事件定义处理程序。

| 1. | utf8_decode() | 将 UTF-8 字符串解码为 ISO-8859-1 |
| 2. | utf8_encode() | 将 ISO-8859-1 字符串编码为 UTF-8 |
| 3. | xml_error_string() | 从 XML 解析器获取一个错误字符串。 |
| 4. | XML _ get _ current _ byte _ index() | 从 XML 解析器获取当前字节索引。 |
| 5. | XML _ get _ current _ column _ number() | 从 XML 解析器获取当前的列号。 |
| 6. | XML _ get _ current _ line _ number() | 从 XML 解析器中获取当前行号 |
| 7. | xml_get_error_code() | 从 XML 解析器获取一个错误代码。 |
| 8. | xml_parse() | 解析一个 XML 文档。 |
| 9. | xml_parse_into_struct() | 将 XML 数据解析成一个数组。 |
| 10. | xml_parser_create_ns() | 创建一个支持名称空间的 XML 解析器。 |
| 11. | xml_parser_create() | 创建一个 XML 解析器 |
| 12. | xml_parser_free() | 释放一个 XML 解析器 |
| 13. | XML _ parser _ get _ 选项() | 从 XML 解析器获取选项 |
| 14. | xml 解析器设置选项() | 在 XML 解析器中设置选项 |
| 15. | XML _ set _ character _ data _ handler() | 设置字符数据的处理函数。 |
| 16. | XML _ set _ default _ handler() | 设置默认处理器功能。 |
| 17. | XML _ set _ element _ handler() | 为元素的开始和结束设置处理函数。 |
| 18. | XML _ set _ end _ namespace _ decl _ handler() | 为名称空间声明的结尾设置处理函数 |
| 19. | XML _ set _ external _ entity _ ref _ handler() | 为外部实体设置处理函数。 |
| 20. | XML _ set _ notation _ decl _ handler() | 为符号声明设置处理函数。 |
| 21. | xml_set_object() | 在对象内使用 XML 解析器。 |
| 22. | XML _ set _ processing _ instruction _ handler() | 设置处理指令的处理函数。 |
| 23. | XML _ set _ start _ namespace _ decl _ handler() | 为命名空间声明的开始设置处理函数 |
| 24. | XML _ set _ un parsed _ entity _ decl _ handler() | 为未解析的实体声明设置处理函数。 |

### **XML 解析器常量**

| 1. | XML_ERROR_NONE(整数) | 2. | XML_ERROR_ASYNC_ENTITY(整数) |
| 3. | XML_ERROR_NO_MEMORY(整数) | 4. | XML _ ERROR _ BAD _ CHAR _ REF(integer) |
| 5. | XML_ERROR_SYNTAX(整数) | 6. | XML _ ERROR _ BINARY _ ENTITY _ REF(integer) |
| 7. | XML_ERROR_NO_ELEMENTS(整数) | 8. | XML _ ERROR _ ATTRIBUTE _ EXTERNAL _ ENTITY _ REF(整数) |
| 9. | XML_ERROR_INVALID_TOKEN(整数) | 10. | XML _ ERROR _ 错位 _XML_PI(整数) |
| 11. | XML_ERROR_UNCLOSED_TOKEN(整数) | 12. | XML _ 错误 _ 未知 _ 编码(整数) |
| 13. | XML_ERROR_PARTIAL_CHAR(整数) | 14. | XML _ ERROR _ INCORRECT _ ENCODING(整数) |
| 15. | XML_ERROR_TAG_MISMATCH(整数) | 16. | XML _ ERROR _ un closed _ CDATA _ SECTION(integer) |
| 17. | XML _ 错误 _ 重复 _ 属性(整数) | 18. | XML _ ERROR _ EXTERNAL _ ENTITY _ HANDLING(整数) |
| 19. | XML _ ERROR _ JUNK _ AFTER _ DOC _ ELEMENT(整数) | 20. | XML_OPTION_CASE_FOLDING(整数) |
| 21. | XML_ERROR_PARAM_ENTITY_REF(整数) | 22. | XML_OPTION_TARGET_ENCODING(整数) |
| 23. | XML_ERROR_UNDEFINED_ENTITY(整数) | 24. | XML_OPTION_SKIP_TAGSTART(整数) |
| 25. | XML _ ERROR _ RECURSIVE _ ENTITY _ REF(integer) | 26. | XML_OPTION_SKIP_WHITE(整数) |

### **MYSQLI 函数**

这些功能允许你访问 MySQL 数据库服务器。

| 1. | mysqli::$affected_rows | 获取上一次 MySQL 操作中受影响的行数 |
| 2. | mysqli::autocommit() | 打开或关闭自动提交数据库修改 |
| 3. | mysqli::change_user() | 改变指定数据库连接的用户。 |
| 4. | MySQL::character _ set _ name() | 返回数据库连接的默认字符集 |
| 5. | mysqli::$client_info | 获取 MySQL 客户端信息 |
| 6. | mysqli::$client_version | 以字符串形式返回 MySQL 客户端版本。 |
| 7. | mysqli::close() | 关闭先前打开的数据库连接。 |
| 8. | mysqli::commit() | 提交当前事务。 |
| 9. | mysqli::$connect_errno | 返回上次连接调用的错误代码。 |
| 10. | mysqli::$connect_error | 返回上一次连接错误的字符串描述。 |
| 11. | mysqli::__construct() | 打开一个到 MySQL 服务器的新连接。 |
| 12. | mysqli::debug() | 执行调试操作。 |
| 13. | mysqli::dump _ debug _ info() | 将调试信息转储到日志中。 |
| 14. | mysqli::$errno | 返回最近一次函数调用的错误代码。 |
| 15. | mysqli::$error_list | 返回上一次执行的命令的错误列表。 |
| 16. | mysqli::$error | 返回上一个错误的字符串描述。 |
| 17. | mysqli::$field_count | 返回最近一次查询的列数。 |
| 18. | mysqli::get_charset() | 返回一个字符集对象。 |
| 19. | mysqli::get _ client _ info() | 获取 MySQL 客户端信息。 |
| 20. | mysqli _ get _ client _ stats() | 返回客户端每个进程的统计数据 |
| 21. | mysqli _ get _ client _ version() | 以字符串形式返回 MySQL 客户端版本。 |
| 22. | mysqli::get _ connection _ stats() | 返回关于客户端连接的统计信息 |
| 23. | mysqli::$host_info | 返回代表所用连接类型的字符串。 |
| 24. | mysqli::$ protocol _ version | 返回使用的 MySQL 协议的版本。 |
| 25. | mysqli::$server_info | 返回 MySQL 服务器的版本。 |
| 26. | mysqli::$server_version | 以整数形式返回 MySQL 服务器的版本。 |
| 27. | mysqli::get_warnings() | 得到“显示警告”的结果。 |
| 28. | mysqli::$info | 检索关于最近执行的查询的信息。 |
| 29. | mysqli::init() | 初始化 MYSQLi 并返回一个与 mysqli_real connect()一起使用的资源 |
| 30. | mysqli::$insert_id | 返回上次查询中使用的自动生成的 id。 |
| 31. | mysqli::kill() | 要求服务器终止一个 MySQL 线程。 |
| 32. | mysqli::more_results() | 检查多重查询是否还有其他查询结果。 |
| 33. | mysqli::multi_query() | 对数据库执行查询。 |
| 34. | mysqli::next_result() | 从 multi_query 准备下一个结果。 |
| 35. | mysqli::options() | 设置选项。 |
| 36. | mysqli::ping() | ping 一个服务器连接，或者在条件出现问题时尝试重新连接。 |
| 37. | mysqli::poll() | 投票连接。 |
| 38. | mysqli::prepare() | 准备要执行的 SQL 语句。 |
| 39. | mysqli::query() | 对数据库执行查询。 |
| 40. | mysqli::real_connect() | 打开与 mysql 服务器的连接。 |
| 41. | mysqli::real _ escape _ string() | 考虑到连接的当前字符集，对 SQL 语句中使用的字符串中的特殊字符进行转义。 |
| 42. | mysqli::real_query() | 执行一个 SQL 查询。 |
| 43. | mysqli::reap _ async _ query() | 从异步查询中获取结果。 |
| 44. | mysqli::refresh() | 刷新 |
| 45. | MySQL::roll back() | 回滚当前事务。 |
| 46. | mysqli::rpl_query_type() | 返回 RPL 查询类型。 |
| 47. | mysqli::select_db() | 选择数据库查询的默认数据库。 |
| 48. | mysqli::send_query() | 发送查询并返回。 |
| 49. | mysqli::set_charset() | 设置默认客户端字符集。 |
| 50. | mysqli::set _ local _ infile _ default() | 取消加载本地文件命令的用户定义处理程序。 |
| 51. | mysqli::set _ local _ infile _ handler() | 加载数据本地文件命令的回调函数。 |
| 52. | mysqli::$sqlstate | 返回上一次 MySQL 操作的 SQLSTATE 错误。 |
| 53. | mysqli::ssl_set() | 用于使用 SSL 建立安全连接 |
| 54. | mysqli::stat() | 获取当前系统状态。 |
| 55. | mysqli::stmt_init() | 初始化一条语句并返回一个对象，用于 mysqli_stmt prepare。 |
| 56. | mysqli::store_result() | 传输上一次查询的结果集。 |
| 57. | mysqli::$thread_id | 返回当前连接的线程 ID。 |
| 58. | mysqli::thread_safe() | 返回是否给定线程安全。 |
| 59. | mysqli::use_result() | 启动结果集检索。 |
| 60. | mysqli::$warning_count | 返回给定链接的最后一次查询的警告数。 |

### **MYSQLI 语句常量**

| 1. | mysqli _ stmt::$ affected _ rows | 返回最后执行的语句更改、删除或插入的总行数。 |
| 2. | mysqli_stmt::attr_get() | 用来获取一个语句属性的当前值。 |
| 3. | mysqli_stmt::attr_set() | 用于修改预准备语句的行为。 |
| 4. | mysqli _ stmt::bind _ param() | 将变量作为参数绑定到准备好的语句。 |
| 5. | mysqli _ stmt::bind _ result() | 将变量绑定到一个准备好的语句，用于结果存储。 |
| 6. | mysqli_stmt::close() | 关闭准备好的语句。 |
| 7. | mysqli_stmt::data_seek() | 查找语句结果集中的任意行。 |
| 8. | mysqli_stmt::$errno | 返回最近一次语句调用的错误代码。 |
| 9. | mysqli_stmt::$error_list | 返回上次执行的语句中的错误列表。 |
| 10. | mysqli_stmt::$error | 返回上一条语句错误的字符串描述。 |
| 11. | mysqli_stmt::execute() | 执行准备好的查询。 |
| 12. | mysqli_stmt::fetch() | 从预准备语句中提取结果到绑定变量中。 |
| 13. | mysqli _ stmt::$ field _ count | 返回给定语句中字段的个数。 |
| 14. | mysqli _ stmt::free _ result() | 为给定的语句句柄释放存储的结果内存。 |
| 15. | mysqli _ stmt::get _ result() | 从准备好的语句中获取结果。 |
| 16. | mysqli _ stmt::get _ warnings() | 获取显示警告的结果 |
| 17. | mysqli_stmt::$insert_id | 获取上一次插入操作生成的 ID。 |
| 18. | mysqli _ stmt::more _ results() | 检查多重查询是否有更多查询结果。 |
| 19. | mysqli _ stmt::next _ result() | 从多重查询中读取下一个结果。 |
| 20. | mysqli_stmt::$num_rows | 返回语句结果集中的行数。 |
| 21. | mysqli _ stmt::$ param _ count | 返回给定语句的参数个数。 |
| 22. | mysqli_stmt::prepare() | 准备要执行的 SQL 语句。 |
| 23. | mysqli_stmt::reset() | 重置准备好的语句。 |
| 24. | MySQL _ stmt::result _ metadata() | 从预准备语句返回结果集元数据。 |
| 25. | mysqli _ stmt::send _ long _ data() | 分块发送数据。 |
| 26. | mysqli_stmt::$sqlstate | 返回上一个语句操作的 SQLSTATE 错误。 |
| 27. | mysqli _ stmt::store _ result() | 从预准备语句传输结果集。 |

### **MYSQLI 结果类**

| 1. | mysqli _ result::$ current _ field | 获取结果指针的当前字段偏移量。 |
| 2. | mysqli _ result::data _ seek() | 将结果指针调整到结果中的任意一行。 |
| 3. | mysqli _ result::fetch _ all() | 以关联数组、数值数组或两者的形式获取所有结果行。 |
| 4. | mysqli _ result::fetch _ array() | 以关联数组、数值数组或两者的形式获取结果行。 |
| 5. | mysqli _ result::fetch _ assoc() | 获取结果行作为关联数组。 |
| 6. | mysqli _ result::fetch _ field _ direct() | 获取单个字段的元数据。 |
| 7. | mysqli _ result::fetch _ field() | 返回结果集中的下一个字段。 |
| 8. | mysqli _ result::fetch _ fields() | 返回表示结果集中字段的对象数组。 |
| 9. | mysqli _ result::fetch _ object() | 将结果 se 的当前行作为对象返回。 |
| 10. | mysqli _ result::fetch _ row() | 获取一个结果行作为枚举数组。 |
| 11. | mysqli _ result::$ field _ count | 获取结果中的字段数。 |
| 12. | mysqli _ result::field _ seek() | 将结果指针设置到指定的字段偏移量。 |
| 13. | mysqli_result::free() | 释放与结果相关的内存。 |
| 14. | mysqli_result::$lengths | 返回结果集中当前行的列的长度。 |
| 15. | mysqli_result::$num_rows | 获取结果中的行数。 |

### **MYSQLI 驱动程序类**

| 1. | mysqli _ driver::embedded _ server _ end() | 停止嵌入式服务器 |
| 2. | mysqli _ driver::embedded _ server _ start() | 初始化并启动嵌入式服务器 |
| 3. | mysqli _ driver::$ report _ mode | 启用或禁用内部报表功能 |
| 4. | mysqli _ driver::$ client _ info | 客户端 API 头文件版本。 |
| 5. | mysqli _ driver::$ client _ version | 客户端版本 |
| 6. | mysqli _ driver::$ driver _ version | MySQLi 驱动程序版本 |
| 7. | mysqli_driver::$embedded | 是否启用 MySQLi 嵌入式支持。 |
| 8. | mysqli _ driver::$ reconnect | 允许或阻止重新连接 |
| 9. | mysqli _ driver::$ report _ mode | 设置为 MYSQLi_REPORT_OFF、MYSQLi_REPORT_ALL 或 MYSQLI_REPORT_STRICT(抛出错误异常)、MYSQLI_REPORT_ERROR(报告错误)和 MYSQLI_REPORT_INDEX(关于索引的错误)的任意组合。 |

### **MYSQLI 警告类**

| 1. | mysqli _ warning::_ _ construct() | _ 构造目的 |
| 2. | mysqli_warning::next() | 下一个目的 |
| 3. | mysqli_warning::$message | 消息字符串 |
| 4. | mysqli _ warning::$ SQLSTATE | SQL 状态 |
| 5. | mysqli_warning::$errno | MySQLi 驱动程序版本 |

### **MYSQLi 常量**

| 1. | MYSQLI _ READ _ DEFAULT _ GROUP | 从 my.cnf 或 MYSQLI_READ_DEFAULT_FILE 指定的文件中读取命名组的选项 |
| 2. | MYSQLI_READ_DEFAULT_FILE | 从已命名的选项文件中读取选项，而不是从 my.cnf 中读取选项 |
| 3. | MYSQLI _ OPT _ CONNECT _ time out | 以秒为单位的连接超时 |
| 4. | MYSQLI_OPT_LOCAL_INFILE | 启用命令加载本地文件 |
| 5. | MYSQLI_INIT_COMMAND | 连接到 MySQL 服务器时执行的命令。将在重新连接时自动重新执行。 |
| 6. | MYSQLI_CLIENT_SSL | 使用 SSL(加密协议)。应用程序不应设置此选项；它在 MySQL 客户端库中内部设置 |
| 7. | MYSQLI_CLIENT_COMPRESS | 使用压缩协议 |
| 8. | MYSQLI _ CLIENT _ INTERACTIVE | 在关闭连接之前，允许不活动的交互超时秒数(而不是等待超时秒数)。客户端的会话 wait_timeout 变量将被设置为会话 interactive_timeout 变量的值。 |
| 9. | MYSQLI _ CLIENT _ IGNORE _ SPACE | 函数名后允许有空格。使所有函数名成为保留字。 |
| 10. | MYSQLI_CLIENT_NO_SCHEMA | 不允许 db_name.tbl_name.col_name 语法。 |
| 11. | MYSQLI _ CLIENT _ MULTI _ query | 允许在一个 mysqli_query()调用中使用多个分号分隔的查询。 |
| 12. | MYSQLI_STORE_RESULT | 用于使用缓冲的结果集 |
| 13. | MYSQLI_USE_RESULT | 用于使用未缓冲的结果集 |
| 14. | MYSQLI_ASSOC | 将列返回到以字段名为数组索引的数组中。 |
| 15. | MYSQLI_NUM | 列被返回到具有枚举索引的数组中。 |
| 16. | MYSQLI_BOTH | 列被返回到既有数字索引又有字段名作为关联索引的数组中。 |
| 17. | MYSQLI_NOT_NULL_FLAG | 表示字段被定义为非空 |
| 18. | MYSQLI_PRI_KEY_FLAG | 字段是主索引的一部分 |
| 19. | MySQL _ UNIQUE _ KEY _ FLAG | 字段是唯一索引的一部分。 |
| 20. | MYSQLI_MULTIPLE_KEY_FLAG | 字段是索引的一部分。 |
| 21. | MYSQLI_BLOB_FLAG | 字段被定义为斑点 |
| 22. | MYSQLI_UNSIGNED_FLAG | 字段被定义为无符号 |
| 23. | MYSQLI_ZEROFILL_FLAG | 字段被定义为零填充 |
| 24. | MYSQLI _ AUTO _ INCREMENT _ FLAG | 字段被定义为自动增量 |
| 25. | MYSQLI_TIMESTAMP_FLAG | 字段被定义为时间戳 |
| 26. | MYSQLI_SET_FLAG | 字段被定义为集合 |
| 27. | MYSQLI_NUM_FLAG | 字段被定义为数字 |
| 28. | MYSQLI_PART_KEY_FLAG | 字段是多索引的一部分 |
| 29. | MYSQLI_GROUP_FLAG | 字段是分组依据的一部分 |
| 30. | MYSQLI_TYPE_DECIMAL | 字段被定义为十进制 |
| 31. | MYSQLI_TYPE_NEWDECIMAL | 精确数学十进制或数值字段(MySQL 5.0.3 及更高版本) |
| 32. | MYSQLI_TYPE_BIT | 字段定义为 BIT (MySQL 5.0.3 及以上) |
| 32. | MYSQLI_TYPE_TINY | 字段被定义为 TINYINT |
| 34. | MYSQLI_TYPE_SHORT | 字段被定义为 SMALLINT |
| 35. | MYSQLI_TYPE_LONG | 字段被定义为 INT |
| 36. | MYSQLI_TYPE_FLOAT | 字段被定义为浮点型 |
| 37. | MYSQLI_TYPE_DOUBLE | 字段被定义为双精度 |
| 38. | MYSQLI_TYPE_NULL | 39. |
| MYSQLI_TYPE_TIMESTAMP | 字段被定义为时间戳 | 40. |
| MYSQLI_TYPE_LONGLONG | 字段被定义为 BIGINT | 41. |
| MYSQLI_TYPE_INT24 | 字段被定义为中间值 | 42. |
| MYSQLI_TYPE_DATE | 字段被定义为日期 | 43. |
| MYSQLI_TYPE_TIME | 字段被定义为时间 | 44. |
| MYSQLI_TYPE_DATETIME | 字段被定义为日期时间 | 45. |
| MYSQLI_TYPE_YEAR | 字段定义为年份 | 46. |
| MYSQLI_TYPE_NEWDATE | 字段被定义为日期 | 47. |
| MYSQLI_TYPE_INTERVAL | 字段被定义为区间 | 48. |
| MYSQLI_TYPE_ENUM | 字段被定义为枚举 | 49. |
| MYSQLI_TYPE_SET | 字段被定义为集合 | 50. |
| MYSQLI_TYPE_TINY_BLOB | 字段被定义为 TINYBLOB | 51. |
| MYSQLI_TYPE_MEDIUM_BLOB | 字段被定义为 MEDIUMBLOB | 52. |
| MYSQLI_TYPE_LONG_BLOB | 字段被定义为 LONGBLOB | 53. |
| MYSQLI_TYPE_BLOB | 字段被定义为斑点 | 54. |
| MYSQLI_TYPE_VAR_STRING | 字段被定义为 VARCHAR | 55. |
| MYSQLI_TYPE_STRING | 字段被定义为字符或二进制 | 56. |
| mysqli _ type _ char | 字段被定义为 TINYINT。关于 CHAR，请参见 MYSQLI_TYPE_STRING | 57. |
| MYSQLI_TYPE_GEOMETRY | 场被定义为几何图形 | 58. |
| MYSQLI_NEED_DATA | 更多数据可用于绑定变量 | 59. |
| MYSQLI_NO_DATA | 绑定变量没有更多可用数据 | 60. |
| MYSQLI_DATA_TRUNCATED | 发生数据截断。从 PHP 5.1.0 和 MySQL 5.0.5 开始可用。 | 61. |
| MYSQLI_ENUM_FLAG | 字段被定义为枚举。从 PHP 5.3.0 开始可用。 | 62. |
| MYSQLI_REPORT_INDEX | 报告查询中是否没有使用索引或使用了错误的索引。 | 63. |
| MYSQLI_REPORT_ERROR | 报告 mysqli 函数调用的错误。 | 64. |
| MYSQLI_REPORT_STRICT | 对于错误而不是警告，抛出一个 mysqli_sql_exception。 | 65. |
| MYSQLI_REPORT_ALL | 将所有选项设置为开(全部报告)。 | 66. |
| MYSQLI_REPORT_OFF | 关闭报告。 | 67. |
| MYSQLI _ DEBUG _ TRACE _ ENABLED | 如果启用了 mysqli_debug()功能，则设置为 1。 | 68. |
| MYSQLI _ SERVER _ QUERY _ NO _ GOOD _ INDEX _ USED |  | 69. |
| MYSQLI _ SERVER _ QUERY _ NO _ INDEX _ USED |  | 70. |
| MYSQLI_REFRESH_GRANT | 刷新授权表。 | 71. |
| MYSQLI_REFRESH_LOG | 刷新日志，类似于执行 FLUSH LOGS SQL 语句。 | 72. |
| MYSQLI_REFRESH_TABLES | 刷新表缓存，类似于执行 FLUSH TABLES SQL 语句。 | 73. |
| MYSQLI_REFRESH_HOSTS | 刷新主机缓存，就像执行刷新主机 SQL 语句一样。 | 74. |
| MYSQLI_REFRESH_STATUS | 重置状态变量，类似于执行 FLUSH STATUS SQL 语句。 | 75. |
| MYSQLI_REFRESH_THREADS | 刷新线程缓存。 | 76. |
| MYSQLI_REFRESH_SLAVE | 在从属复制服务器上:重置主服务器信息，并重启从属服务器。比如执行 RESET SLAVE SQL 语句。 | 77. |
| MYSQLI_REFRESH_MASTER | 在主复制服务器上:删除二进制日志索引中列出的二进制日志文件，并截断索引文件。比如执行 RESET MASTER SQL 语句。 | **杂项功能** |

### 所有其他分类的职能都被归入这一类别。这些函数的行为受到 php.ini 文件中设置的影响。

1.

| 连接 _ 中止() | 检查客户端是否已断开连接。 | 2. |
| 连接状态() | 返回当前连接状态 | 3. |
| 连接 _ 超时() | 从 PHP 4.0.5 开始弃用 | 4. |
| 常数() | 返回常量的值。 | 5. |
| define() | 定义了一个常数。 | 6. |
| 已定义() | 检查常量是否存在。 | 7. |
| die() | 打印信息并退出当前脚本 | 8. |
| eval() | 将字符串计算为 PHP 代码 | 9. |
| 退出() | 打印信息并退出当前脚本。 | 10. |
| get_browser() | 返回用户浏览器的功能 | 11. |
| 高亮 _ 文件() | 输出一个 PHP 语法高亮显示的文件 | 12. |
| highlight_string() | 输出一个字符串，突出显示 PHP 语法。 | 13. |
| ignore_user_abort() | 设置远程客户端是否可以中止脚本的运行。 | 14. |
| pack() | 将数据打包成二进制字符串 | 15. |
| php_strip_whitespace() | 从文件的源代码中删除空格和 PHP 注释。 | 16. |
| show_source() | 高亮文件()的别名 | 17. |
| 睡眠() | 延迟代码执行几秒钟。 | 18. |
| time_nanosleep() | 将代码执行延迟几秒和几纳秒。 | 19. |
| time_sleep_until() | 将代码执行延迟到指定的时间。 | 20. |
| uniqid() | 生成唯一 ID | 21. |
| unpack() | 从二进制字符串中解包数据。 | 22. |
| usleep() | 将代码执行延迟几微秒。 | **杂项常数** |

### 1.

| 连接 _ 中止 | 连接被用户或网络错误中止。 | 2. |
| 连接 _ 正常 | 连接运行正常。 | 3. |
| 连接 _ 超时 | 连接超时。 | 4. |
| _ _ 编译器 _ 暂停 _ 偏移 __ | 决定数据开始的字节位置。 | **面向对象编程** |

### PHP 代码也可以用面向对象的格式编写。OOP 执行起来更快更容易。OOP 结构使得代码更容易维护、修改和调试。

1.

| __construct() | 具有构造函数方法的类在每个新创建的对象上调用这个方法，因此它适用于对象在使用前可能需要的任何初始化。 | 2. |
| __destruct() | 一旦没有对特定对象的其他引用，就调用，或者在关闭序列中以任何顺序调用。 | 3. |
| __callStatic() | 在静态上下文中调用不可访问的方法时触发。 | 4. |
| __call() | 在对象上下文中调用不可访问的方法时触发。 | 5. |
| __get() | 用于从不可访问的属性中读取数据。 | 6. |
| __set() | 向不可访问的属性写入数据时运行。 | 7. |
| __isset() | 通过对不可访问的属性调用 isset()或 empty()触发。 | 8. |
| __unset() | 在不可访问的属性上使用 unset()时调用。 | 9. |
| __sleep() | _sleep()的预期用途是提交待定数据或执行类似的清理任务。此外，如果您有不需要完全保存的非常大的对象，该函数也很有用。 | 10. |
| __wakeup() | 用于重新建立序列化过程中可能丢失的数据库连接，并执行其他重新初始化任务。 | 11. |
| __toString() | 允许一个类决定当它被当作一个字符串时将如何反应。 | 12. |
| __invoke() | 当脚本试图调用一个对象作为函数时调用。 | 13. |
| __set_state() | 从 PHP 5.1.0 开始调用 var_export()导出的类 | 14. |
| __clone() | 一旦克隆完成，如果定义了 _clone()方法，那么新创建的对象的 _clone()方法将被调用，以允许任何需要改变的必要属性。 | **误差函数** |

### 这些函数用于处理错误和记录日志。记录功能允许直接向其他机器或系统发送消息，而错误报告功能允许定制错误级别和给定的反馈。错误函数的行为受到 php.ini 中设置的影响

1.

| debug_backtrace() | 生成回溯 | 2. |
| debug_print_backtrace() | 打印回溯 | 3. |
| error_get_last() | 获取最后发生的错误 | 4. |
| error_log() | 将错误发送到服务器错误日志、文件或远程目的地。 | 5. |
| 错误报告() | 指定报告哪些错误。 | 6. |
| 还原错误处理函数() | 恢复之前的错误处理程序 | 7. |
| 恢复 _ 异常 _ 处理程序() | 恢复之前的异常处理程序 | 8. |
| set_error_handler() | 设置用户定义的函数来处理错误。 | 9. |
| set_exception_handler() | 设置用户定义的函数来处理异常。 | 10. |
| trigger_error() | 创建用户定义的错误信息。 | 11. |
| user_error() | 触发错误别名。 | **误差常数** |

### 1.

| E_ERROR1 | 致命的运行时错误。无法恢复的错误。暂停脚本的执行 | 2. |
| 电子警告 2 | 非致命运行时错误。脚本的执行没有停止 | 2. |
| E_PARSE4 | 编译时解析错误。解析错误应该只由解析器生成 | 3. |
| 电子公告 8 | 运行时通知。脚本发现了一些可能是错误的东西，但在正常运行脚本时也可能发生 | 4. |
| E_CORE_ERROR16 | PHP 启动时的致命错误。这就像 PHP 内核中的 E _ ERROR | 5. |
| E_CORE_WARNING32 | PHP 启动时的非致命错误。这就像 PHP 核心中的 E _ WARNING | 6. |
| E_COMPILE_ERROR64 | 致命的编译时错误。这就像 Zend 脚本引擎生成的 E _ ERROR】 | 7. |
| E_COMPILE_WARNING128 | 非致命的编译时错误。这就像 Zend 脚本引擎生成的 E_WARNING | 8. |
| E_USER_ERROR256 | 致命的用户生成的错误。这就像程序员使用 PHP 函数 trigger_error() 设置的 E_ERROR | 9. |
| E_USER_WARNING512 | 用户生成的非致命警告。这就像程序员使用 PHP 函数 trigger_error() 设置的 E_WARNING | 10. |
| 电子用户通知 1024 | 用户生成的通知。这就像程序员使用 PHP 函数 trigger_error() 设置的 E_NOTICE | 11. |
| E_STRICT2048 | 运行时通知。PHP 建议修改你的代码以帮助代码的互操作性和兼容性 | 12. |
| E_RECOVERABLE_ERROR4096 | 可捕捉的致命错误。这类似于一个 E_ERROR，但是可以被用户定义的句柄捕获(参见 set_error_handler()) | 13. |
| E_ALL6143 | 所有错误和警告，除了等级 E_STRICT | **人也在读:** |

**People are also reading:**