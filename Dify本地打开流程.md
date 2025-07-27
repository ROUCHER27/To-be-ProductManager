### 每次启动 Dify 的标准流程 (SOP)

为了回答您的第二个问题，这里是您以后每次（比如重启电脑后）想要访问 Dify 时，需要遵循的完整流程。您需要打开 **3个** 终端窗口。

#### ✅ **终端窗口 1：启动后端 API 服务**

1. 打开一个新的终端窗口。
    
2. 进入 `api` 目录：`cd ~/Desktop/AI1/dify/api`
    
3. 激活虚拟环境：`source .venv/bin/activate`
    
4. 启动服务：`flask run --host=0.0.0.0 --port=5001`
    
5. **让这个窗口保持运行，不要关闭。**
    

#### ✅ **终端窗口 2：启动后端 Worker 服务**

1. 打开**第二个**新的终端窗口。
    
2. 进入 `api` 目录：`cd ~/Desktop/AI1/dify/api`
    
3. 激活虚拟环境：`source .venv/bin/activate`
    
4. 启动服务：`celery -A app.celery worker -P gevent -c 1 --loglevel INFO -Q dataset,generation,mail,ops_trace`
    
5. **让这个窗口也保持运行，不要关闭。**
    

#### ✅ **终端窗口 3：启动前端 Web 服务**

1. 打开**第三个**新的终端窗口。
    
2. 进入 `web` 目录：`cd ~/Desktop/AI1/dify/web`
    
3. 启动服务：`pnpm dev`
    
4. **让这个窗口也保持运行，不要关闭。**
    

#### ✅ **最后一步：访问应用**

当以上三个服务都在各自的终端里成功运行后，打开您的浏览器，访问 `http://localhost:3000`。

---

请先按照【第一部分】的步骤来修复您损坏的虚拟环境。一旦成功，您以后就可以一直使用【第二部分】的“标准流程”来启动 Dify 了。