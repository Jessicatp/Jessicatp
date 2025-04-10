<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>岗位详情</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        .job-detail {
            padding: 20px;
            background-color: white;
            margin: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .job-detail h2 {
            margin: 0;
            font-size: 24px;
            color: #333;
        }
        .job-detail p {
            margin: 10px 0;
            color: #666;
        }
        .job-detail .section {
            margin-top: 20px;
        }
        .job-detail .section h3 {
            margin: 0;
            font-size: 18px;
            color: #333;
        }
        .job-detail .section p {
            margin: 5px 0;
            color: #666;
        }
        .buttons {
            display: flex;
            justify-content: space-around;
            margin-top: 30px;
        }
        .buttons button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #007bff;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }
        .buttons button.share {
            background-color: #28a745;
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            text-align: center;
        }
        .modal-content img {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="job-detail">
        <h2>前端开发工程师</h2>
        <p>工作地点：北京</p>
        <p>薪资：15K-25K</p>
        <div class="section">
            <h3>任职资格</h3>
            <p>1. 本科及以上学历，计算机相关专业；</p>
            <p>2. 3年以上前端开发经验；</p>
            <p>3. 熟悉HTML、CSS、JavaScript等前端技术；</p>
        </div>
        <div class="section">
            <h3>岗位要求</h3>
            <p>1. 负责公司前端项目的开发与维护；</p>
            <p>2. 与设计师、后端工程师紧密合作，完成产品开发；</p>
            <p>3. 持续优化前端性能，提升用户体验。</p>
        </div>
        <div class="buttons">
            <button class="share" onclick="shareJob()">分享</button>
            <button onclick="showQRCode()">投递</button>
        </div>
    </div>
    <div class="modal" id="qrModal">
        <div class="modal-content">
            <img src="wechat_qr.png" alt="微信二维码">
            <p>扫描二维码投递简历</p>
            <button onclick="closeQRCode()">关闭</button>
        </div>
    </div>
    <script>
        function showQRCode() {
            document.getElementById('qrModal').style.display = 'flex';
        }
        function closeQRCode() {
            document.getElementById('qrModal').style.display = 'none';
        }
        function shareJob() {
            alert('请点击微信右上角按钮进行分享。');
        }
    </script>
</body>
</html>
