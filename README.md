<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>法鼓山活動行前確認</title>

<style>
body {
  font-family: "Noto Sans TC","Microsoft JhengHei",sans-serif;
  background-image: url('https://fagushan.ddm.org.tw/files/file_pool/1/0M005733797053262001/P75420150204010005s2.jpg');
  background-size: cover;
  background-attachment: fixed;
  background-position: center;
  margin: 0;
  padding: 20px;
  line-height: 1.8;
}

/* 毛玻璃卡片 */
.card {
  background: rgba(255,255,255,0.8); /* 稍微調高不透明度，讓字體更清晰 */
  backdrop-filter: blur(8px);
  border-radius: 18px;
  box-shadow: 0 10px 35px rgba(0,0,0,0.25);
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

/* --- 大字模式修正 --- */
.elder {
  font-size: 1.4em !important; /* 增加強制性 */
  line-height: 2.2 !important;
}

.elder h1 { font-size: 40px !important; }
.elder h2 { font-size: 32px !important; }
.elder h3 { font-size: 28px !important; }
.elder h4 { font-size: 26px !important; }
.elder li, .elder span, .elder label {
  font-size: 1.2em !important;
  font-weight: 700 !important;
}
.elder input[type="checkbox"] {
  transform: scale(1.8) !important; /* 勾選框也加大 */
  margin-right: 15px;
}

/* 標題 */
h1 { color: #b00020; text-align: center; margin-top: 0; }
h2 { text-align: center; border-bottom: 2px solid #ddd; padding-bottom: 10px; }

h3 {
  background: #f3f3f3;
  padding: 10px 15px;
  border-left: 5px solid #b00020;
  margin-top: 25px;
}

/* 列表樣式 */
ul { list-style: none; padding-left: 10px; }
li { margin-bottom: 15px; }

label {
  display: flex;
  align-items: center;
  cursor: pointer;
}

input[type="checkbox"] {
  margin-right: 10px;
  transform: scale(1.3);
}

input[type="checkbox"]:checked + span {
  text-decoration: line-through;
  color: #888;
}

/* 按鈕 */
.btn-container {
  text-align: center;
  margin: 25px 0;
}

button {
  background-color: #b00020;
  color: white;
  border: none;
  padding: 12px 24px;
  margin: 5px;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
  font-weight: bold;
}

button:hover {
  background-color: #7d0016;
}

/* 底部圖片 */
.footer-img {
  text-align: center;
  margin-top: 30px;
  border-top: 1px solid #ccc;
  padding-top: 20px;
}

.footer-img img {
  width: 100%;
  max-width: 100%;
  border-radius: 12px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.2);
}
</style>
</head>

<body>

<div class="card" id="mainCard">

    <h1>法鼓山寶雲寺 朝山菩薩</h1>
    <h2>04/18～04/19「朝山・巡禮・憶師恩」</h2>

    <div class="btn-container">
      <button onclick="toggleElder()">👴 切換大字模式</button>
      <button onclick="resetChecks()">🔄 清除勾選</button>
    </div>

    <h3>📌 行前提醒</h3>
    <ul>
        <li>
          <span style="color:red; font-weight:bold;">⚠️ 依車長通知之時間地點集合，準時出發（逾時不候）</span>
        </li>
        <li>💡 請使用後背包，以利行走。</li>
    </ul>

    <h3>✅ 行前確認清單</h3>

    <h4>🍱 餐食準備</h4>
    <ul>
      <li><label><input type="checkbox"><span>早齋需自理 (車上不提供)</span></label></li>
      <li><label><input type="checkbox"><span>自備湯匙或筷子 (★不必帶便當盒)</span></label></li>
    </ul>

    <h4>🛏️ 住宿與個人物品</h4>
    <ul>
      <li><label><input type="checkbox"><span>已準備後背包</span></label></li>
      <li><label><input type="checkbox"><span>已準備睡袋</span></label></li>
      <li><label><input type="checkbox"><span>已準備拖鞋</span></label></li>
      <li><label><input type="checkbox"><span>已準備沐浴乳、洗髮精</span></label></li>
      <li><label><input type="checkbox"><span>已準備牙刷、牙膏、毛巾</span></label></li>
      <li><label><input type="checkbox"><span>已準備水杯、雨具</span></label></li>
      <li><label><input type="checkbox"><span><strong>白色透明雨衣（朝山必備）</strong></span></label></li>
      <li><label><input type="checkbox"><span>已準備遮陽帽、外套、保暖衣物</span></label></li>
      <li><label><input type="checkbox"><span>已準備替換衣物</span></label></li>
      <li><label><input type="checkbox"><span>已攜帶健保卡、個人藥品</span></label></li>
    </ul>

    <h4>👕 服裝確認</h4>
    <ul>
      <li><label><input type="checkbox"><span>已準備樸素衣褲</span></label></li>
      <li><label><input type="checkbox"><span>已準備義工服 (出坡義工)</span></label></li>
    </ul>

    <div class="footer-img">
      <img src="https://raw.githubusercontent.com/dior85200/DDM-checklist/main/朝山日程表.jpg" alt="朝山日程表">
      <p>🗓️ 朝山日程表</p>
    </div>

</div> <script>
// 切換長輩模式
function toggleElder() {
  const card = document.getElementById("mainCard");
  card.classList.toggle("elder");
}

// 清除勾選
function resetChecks() {
  if(confirm("確定要清除所有已勾選的項目嗎？")) {
    document.querySelectorAll("input[type=checkbox]").forEach(cb => cb.checked = false);
  }
}
</script>

</body>
</html>
