## Repository Files Description

Below is the description of the primary Python scripts and their functions in this repository:

### `embddings_process.py`
- **trans_bin**: 将文本格式的词向量文件转换为二进制格式，以加快加载速度。
- **get_new_dict**: 构建新的词典和词向量矩阵，包括处理特殊词向量和失败的词项。
- **get_index**: 根据词典将文本中的词转换为对应的索引值。
- **serialization**: 序列化处理训练、测试、验证数据，以便于模型训练和评估使用。
- **主函数**: 设置文件路径和参数，调用上述函数进行数据处理和序列化操作。

### `getStru2Vec.py`
- **multipro_python_query**: 处理Python查询解析。
- **multipro_python_code**: 处理Python代码解析。
- **multipro_python_context**: 处理Python上下文解析，对特殊标记进行处理。
- **multipro_sqlang_query**: 处理SQL查询解析。
- **multipro_sqlang_code**: 处理SQL代码解析。
- **multipro_sqlang_context**: 处理SQL上下文解析，对特殊标记进行处理。
- **parse**: 使用多进程处理方式解析数据。
- **main**: 综合处理不同类型数据的主函数，包括加载数据、调用解析函数、保存结果。
- **if name == 'main'**: 程序的入口，调用main函数处理具体的数据文件。

### `process_single_corpus.py`
- **load_pickle**: 读取指定路径的pickle二进制文件，并返回数据。
- **split_data**: 根据问题ID将数据分为单候选和多候选两部分。
- **data_staqc_processing**: 处理staqc数据集，根据问题ID分类，并将结果保存到不同的文件。
- **data_large_processing**: 处理大型数据集，根据问题ID分类，并将结果保存到不同的文件。
- **single_unlabeled_to_labeled**: 将未标记的单候选数据转换为带标签的格式，并按问题ID排序后保存。

### `python_structured.py`
- **repair_program_io**: 修复代码中的输入输出格式问题。
- **get_vars**: 使用抽象语法树（AST）从代码中提取变量名。
- **get_vars_heuristics**: 当标准解析失败时，使用启发式方法从代码中提取变量名。
- **PythonParser**: 解析Python代码为令牌序列，执行变量名解析，并处理潜在的解析错误。
- **revert_abbrev**: 将英文缩写还原为完整形式。
- **get_wordpos**: 根据词性标签返回对应的WordNet词性。
- **process_nl_line**: 对自然语言文本行进行预处理，包括还原缩写、命名风格转换和去除括号内容。
- **process_sent_word**: 对文本进行分词、词性标注和词形还原。
- **filter_all_invachar**: 过滤掉Python代码中的非常用字符。
- **filter_part_invachar**: 过滤掉部分特殊字符以减少解析错误。
- **python_code_parse**: 解析Python代码查询，进行文本预处理和令牌化。
- **python_query_parse**: 对Python查询进行预处理和令牌化。
- **python_context_parse**: 对Python上下文进行预处理和令牌化。

### `sqlang_structured.py`
- **tokenizeRegex**: 使用正则表达式扫描器对字符串进行分词。
- **sanitizeSql**: 清理和标准化输入的SQL语句。
- **parseStrings**: 对SQL语句中的字符串进行解析和处理。
- **renameIdentifiers**: 对SQL语句中的标识符进行重命名。
- **removeWhitespaces**: 移除SQL语句中的多余空格。
- **identifyLiterals**: 识别SQL语句中的字面量。
- **identifySubQueries**: 识别SQL语句中的子查询。
- **identifyFunctions**: 识别SQL语句中的函数。
- **identifyTables**: 识别SQL语句中的表和列。
- **getTokens**: 从解析后的SQL语句中提取令牌。
- **revert_abbrev**: 还原英文缩写到完整形式。
- **get_wordpos**: 根据词性标签返回对应的WordNet词性。
- **process_nl_line**: 对自然语言文本行进行预处理，包括还原缩写、命名风格转换、去除括号内容等。
- **process_sent_word**: 对文本进行分词、词性标注和词形还原。
- **filter_all_invachar**: 过滤掉SQL代码中的非常用字符。
- **filter_part_invachar**: 过滤掉SQL代码中部分特殊字符。
- **sqlang_code_parse**: 解析SQL代码查询，进行文本预处理和令牌化。
- **sqlang_query_parse**: 对SQL查询进行预处理和令牌化。
- **sqlang_context_parse**: 对SQL上下文进行预处理和令牌化。
