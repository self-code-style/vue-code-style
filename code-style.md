# 注意事项

```
在使用时需要的前提是项目中安装了以下的node_modules，在开发时才能生效。
"@vue/cli-plugin-babel": "^3.10.0",
"@vue/cli-plugin-eslint": "^3.10.0",
"@vue/cli-service": "^3.10.0",
"@vue/eslint-config-prettier": "^5.0.0",
"babel-eslint": "^10.0.1",
"eslint": "^5.16.0",
"eslint-plugin-prettier": "^3.1.0",
"eslint-plugin-vue": "^5.0.0",
"prettier": "^1.18.2"

编辑器vscode，Extensions: eslint、prettier、vetur
```

# setting.json 文件的配置

```
{
  //.vue文件template格式化支持，并使用js-beautify-html插件
  "vetur.format.defaultFormatter.html": "js-beautify-html",
  //js-beautify-html格式化配置，属性强制换行
  //文档：https://github.com/beautify-web/js-beautify#css--html
  "vetur.format.defaultFormatterOptions": {
    "js-beautify-html": {
      "wrap_attributes": "force"
    }
  },
  //根据文件后缀名定义vue文件类型
  "files.associations": {
    "*.vue": "vue"
  },
  // 保存时eslint自动修复错误
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    {
      "language": "vue",
      "autoFix": true
    }
  ],
  "eslint.autoFixOnSave": true,
  // 保存的时候format
  "editor.formatOnSave": true,
  // tab的空格
  "editor.tabSize": 2,
  // vetur格式化的时候tab距离
  "vetur.format.options.tabSize": 2
}
```

# .prettierrc 文件的配置

```
{
  "eslintIntegration": true,
  //使用单引号
  "singleQuote": true,
  //结尾不加分号
  "semi": false
}
```
