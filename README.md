# [fis-parser-wii-sass](https://github.com/qinmudi/fis-parser-wii-sass) 
fis-parser-wii-sass

## 特色
1、sass预编译无需引入variables和mixins  
2、根据模块自动分发，h5对应找h5的variables和mixins，web自动找web端variables和mixins  
3、支持自定义variables和mixins  
4、下一版本会支持多variables和多mixins支持，如下所示：
```
variables: {
    mobile: [
    	'static/ui/wii-h5/scss/variables1.scss',
    	'static/ui/wii-h5/scss/variables2.scss'
    ],
    web: [
    	'static/ui/wii-web/scss/settings/_settings1.scss',
    	'static/ui/wii-web/scss/settings/_settings2.scss'
    ]
},
mixins: {
    mobile: [
    	'static/ui/wii-h5/scss/mixins1.scss',
    	'static/ui/wii-h5/scss/mixins2.scss'
    ],
    web: [
    	'static/ui/wii-web/scss/util/_mixins1.scss',
    	'static/ui/wii-web/scss/util/_mixins2.scss'
    ]
}
```

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