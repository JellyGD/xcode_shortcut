
# 使用代码片段仓库

命令行进入到代码片段存储的位置：`~/Library/Developer/Xcode/UserData` 

执行以下命令即可：

`
git clone git@github.com:JellyGD/xcode_shortcut.git
`
将代码片段拷贝到 CodeSnippets 目录下。 如果没有CodeSnippets目录则手动创建CodeSnippets目录

`mv  ./xcode_shortcut/*  ./CodeSnippets`

然后重启Xcode即可，Xcode重启后会查找添加的代码片段即可使用。

目前提供几个代码片段：

快捷代码：`tdd`  

描述： tableView 的Delegate和DataSource

```objc
#pragma mark - UITableViewDelegate, UITableViewDataSource

- (NSInteger)numberOfSectionsInTableView:(UITableView *)tableView {
    return <#number#>;
}

- (CGFloat)tableView:(UITableView *)tableView heightForFooterInSection:(NSInteger)section {
    return <#number#>;
}

- (CGFloat)tableView:(UITableView *)tableView heightForHeaderInSection:(NSInteger)section {
    return <#number#>;
}

- (NSInteger)tableView:(UITableView *)tableView numberOfRowsInSection:(NSInteger)section {
    return <#number#>;
}
- (CGFloat)tableView:(UITableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath {
    NSInteger row = indexPath.row;
    NSInteger section = indexPath.section;
    return <#number#>;
}
- (UITableViewCell *)tableView:(UITableView *)tableView cellForRowAtIndexPath:(NSIndexPath *)indexPath {
    NSInteger section = indexPath.section;
    NSInteger row = indexPath.row;
    UITableViewCell *cell;
    
    return cell;
}
- (void)tableView:(UITableView *)tableView didSelectRowAtIndexPath:(NSIndexPath *)indexPath {
    DLog(@"");
}
```
---
快捷代码：`nab` 
描述： BOOL 类型的Property 声明

```objc
/** <#注释#> */
@property(nonatomic, assign) BOOL <#name#>;
```
---
快捷代码：`nc` 
描述： Copy的Property的声明

```objc
/** <#注释#> */
@property(nonatomic,copy) NSString *<#name#>;
```

---
快捷代码：`na` 
描述： assign的Property声明

```objc
/** <#注释#> */
@property(nonatomic, assign) <#class#> <#name#>;

```

---
快捷代码：`ncb` 
描述： Block 类型的Property 声明

```objc
/** <#注释#> */
@property(nonatomic, copy) <#MyBlock#> <#blockName#>;

```

---
快捷代码：`nw` 
描述： weak 类型的Property 声明

```objc
/** <#注释#> */
@property(nonatomic, weak) <#class#> *<#name#>;

```

---
快捷代码：`lg` 
描述：懒加载Getter 

```objc
- (<#class#> *)<#name#> {
    if (!_<#name#>) {
        _<#name#> = [[<#class#> alloc] init];
    }
    return _<#name#>;
}

```
