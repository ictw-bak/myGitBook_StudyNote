# Splash\_Lua脚本

```
function main(splash,args)
    splash:go("https://www.baidu.com")
    input=splash:select("#kw")
    input:send_text("Splash")
    submit=splash:select("#su")
    submit.mouse_click()
    splash:wait(3)
    return splash:png()
end

```



