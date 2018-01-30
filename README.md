# es6-study
# es6环境安装(需要node环境，npm安装器)
1.
 创建项目：项目结构  appName|
                        -- dist  // 存放es6转换后的js文件
                        -- src  // 项目内容
                        .babelrc // es6转换器配置文件
                        .gitignore
                        README.md
2.
 初始化项目
    $ npm install -y
 最新转码规则
    $ npm install --save-dev babel-preset-latest   //  √

 react 转码规则
    $ npm install --save-dev babel-preset-react

 不同阶段语法提案的转码规则（共有4个阶段），选装一个
    $ npm install --save-dev babel-preset-stage-0
    $ npm install --save-dev babel-preset-stage-1
    $ npm install --save-dev babel-preset-stage-2
    $ npm install --save-dev babel-preset-stage-3  // √

3.
 根据安装的插件，修改.babelrc文件
{
    "presets":[
      "latest",
      "stage-3"
    ],
    "plugins":[]
}

4.
 项目中安装 babel-cli
    $ npm install --save-dev babel-cli

5.
 修改package.json, "scripts"属性改为如下，如果没有该属性需要手动添加
"scripts": {
    "build": "babel src -d dist"  // 将编译后的文件放入dist目录
  },