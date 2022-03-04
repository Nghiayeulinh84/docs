每当工作流程中的作业开始时，都会将 `GITHUB_TOKEN` 密钥设置为仓库的访问令牌。 {% ifversion fpt or ghes > 3.1 or ghae or ghec %}您应该在工作流程文件中设置此访问令牌的权限，以授予 `contents` 范围的读取访问权限，并授予 `packages` 范围的写入访问权限。 {% else %}它对工作流程运行的仓库中的包具有读取和写入权限。 {% endif %} 更多信息请参阅“[使用 GITHUB_TOKEN 验证身份](/actions/configuring-and-managing-workflows/authenticating-with-the-github_token)”。