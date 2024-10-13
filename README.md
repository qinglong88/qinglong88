<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>青龙研究院</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
            line-height: 1.6;
        }
        h1 {
            font-size: 26px;
            color: #333;
        }
        p {
            font-size: 20px;
            color: #555;
        }
        #manual-instructions {
            display: none;
        }
        #copy-success {
            display: none;
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 5px;
        }
        button {
            background-color: #008CBA;
            color: white;
            padding: 12px 24px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #005f73;
        }
    </style>
    <script type="text/javascript">
        function tryRedirect() {
            var jumpTo = "https://sway.cloud.microsoft/HrxIdGYgCw4z48vD?ref=Link";
            var isWeixin = navigator.userAgent.toLowerCase().indexOf('micromessenger') !== -1;

            if (isWeixin) {
                document.getElementById("manual-instructions").style.display = "block"; 
            } else {
                window.location.href = jumpTo;
            }
        }

        function copyLink() {
            var link = "https://sway.cloud.microsoft/HrxIdGYgCw4z48vD?ref=Link";
            navigator.clipboard.writeText(link).then(function() {
                var copySuccess = document.getElementById("copy-success");
                copySuccess.style.display = "block";
                setTimeout(function() {
                    copySuccess.style.display = "none";
                }, 3000);
            }).catch(function(error) {
                console.error("复制失败: ", error);
            });
        }

        window.onload = tryRedirect;
    </script>
</head>
<body>
    <h1>青龙研究院</h1>
    <p>如果页面没有自动跳转，说明微信限制了外部链接访问。</p >

    <!-- 手动操作引导区域 -->
    <div id="manual-instructions">
        <h2>在外部浏览器中打开页面</h2>
        <p>1. 点击微信右上角的 <strong>三个点</strong> 图标（右上角）。</p >
        <p>2. 选择 <strong>“在浏览器中打开”</strong> 选项。</p >
        <p>3. 或者，您可以点击以下按钮复制链接，粘贴到浏览器中打开：</p >
        <button onclick="copyLink()">复制链接</button>
    </div>

    <!-- 复制成功提示 -->
    <div id="copy-success">链接已复制！</div>
</body>
</html>
