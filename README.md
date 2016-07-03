# [fis-parser-wii-sass](https://github.com/qinmudi/fis-parser-wii-sass) 
fis-parser-wii-sass

## 特色
1、sass预编译无需引入variables和mixins
2、根据模块自动分发，h5对应找h5的variables和mixins，web自动找web端variables和mixins
3、后续版本支持 fis-conf.json 扩展自定义variables和mixins路径支持

## 说明文档
- 如何使用
```bash
sudo npm i -g fis-parser-wii-sass
```

二、在 fis-conf文件中配置
```bash
fis.match('*.scss', {
    parser: fis.plugin('wii-sass', {
        include_paths: ['static/ui/wii-h5/scss', 'static/ui/wii-web/scss', 'components'],
        variables: {
	        mobile: 'static/ui/wii-h5/scss/variables.scss',
	        web: 'static/ui/wii-web/scss/settings/_settings.scss'
	    },
	    mixins: {
	        mobile: 'static/ui/wii-h5/scss/mixins.scss',
	        web: 'static/ui/wii-web/scss/util/_mixins.scss'
	    }
    })
});
```