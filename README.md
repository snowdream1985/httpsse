# httpsse
Http Server-Sent Events 服务

# 访问地址
http://127.0.0.1:8080/

# javascript示例代码
    const sse = new EventSource("http://127.0.0.1:8080");
    /*
     * 定时心跳
     */
    sse.addEventListener("heartbeat", (e) => {
        console.log(e.data);
    });

    /*
     * 消息
     */
    sse.addEventListener("message", (e) => {
        console.log(e.data);
    });
