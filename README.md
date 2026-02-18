<!DOCTYPE html> 
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio - กฤษฎา ฉัตรกั้น</title>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Kanit',sans-serif}
    body{background:#0b1f14;color:white; scroll-behavior: smooth;}

    nav{
      position:fixed;
      top:0;
      width:100%;
      background:#0f2e1f;
      border-bottom:1px solid #2ecc71;
      display:flex;
      justify-content:center;
      gap:40px;
      padding:15px;
      z-index:1000;
    }

    nav a{
      color:white;
      text-decoration:none;
      font-weight:600;
      transition:.3s;
    }

    nav a:hover{color:#2ecc71;text-shadow:0 0 10px #2ecc71}

    header{
      height:100vh;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      text-align:center;
      background:linear-gradient(135deg,#0b1f14,#0f2e1f,#1e5631);
    }

    h1{font-size:60px;color:#2ecc71;text-shadow:0 0 20px #2ecc71}
    h2{margin-top:10px;color:#dff5e6;font-weight:300}

    section{padding:100px 20px}

    .card{
      background:#0f2e1f;
      border:1px solid #2ecc71;
      border-radius:20px;
      padding:30px;
      margin:30px auto;
      max-width:1000px;
      box-shadow:0 0 30px rgba(46,204,113,0.25);
    }

    .title{font-size:30px;margin-bottom:20px;color:#2ecc71}

    .gallery{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:20px;
    }

    .work{
      background:#133d2a;
      border-radius:15px;
      padding:15px;
      border:1px solid #2ecc71;
      text-align:center;
      transition: transform 0.3s;
    }
    
    .work:hover { transform: translateY(-5px); }

    .work img{
      width:100%;
      height:180px;
      object-fit:cover;
      border-radius:10px;
      margin-bottom:10px;
      background: #0b1f14; /* สีพื้นหลังกรณีไม่มีรูป */
    }

    input,textarea{
      width:100%;
      padding:10px;
      margin-top:10px;
      border-radius:10px;
      border:none;
      background:#1e5631;
      color:white;
    }

    .btn-add{
      margin-top:10px;
      padding:10px 20px;
      border:none;
      border-radius:10px;
      background:#2ecc71;
      color:#0b1f14;
      font-weight:600;
      cursor:pointer;
      width: 100%;
    }

    .skills span{
      display:inline-block;
      background:#2ecc71;
      padding:8px 14px;
      border-radius:999px;
      margin:5px;
      color:#0b1f14;
      font-weight:600;
    }

    footer{text-align:center;padding:40px;color:#a8e6c2}
    
    .btn-delete {
      background:#ff4d4d;
      color:white;
      border:none;
      padding:6px 12px;
      margin-top:8px;
      border-radius:6px;
      cursor:pointer;
      font-size: 14px;
    }
  </style>
</head>
<body>

<nav>
  <a href="#home">หน้าแรก</a>
  <a href="#works">ผลงานของฉัน</a>
  <a href="#about">เกี่ยวกับฉัน</a>
  <a href="#skills">ทักษะ</a>
  <a href="#contact">ติดต่อฉัน</a>
</nav>

<header id="home">
  <h1>PORTFOLIO</h1>
  <h2>กฤษฎา ฉัตรกั้น</h2>
  <h2>ม.4/3 เลขที่ 1</h2>
</header>

<section id="works">
  <div class="card">
    <div class="title">ผลงานของฉัน</div>

    <div class="gallery" id="gallery"></div>

    <hr style="margin: 30px 0; border: 0.5px solid #2ecc71; opacity: 0.3;">
    
    <h3 style="margin-top:20px; color:#2ecc71">➕ เพิ่มผลงานใหม่</h3>
    <input type="text" id="workTitle" placeholder="ชื่อผลงาน (จำเป็น)">
    <input type="file" id="workImage" accept="image/*">
    <input type="text" id="workLink" placeholder="ลิ้งส่งครู / Google Drive / YouTube">
    <button class="btn-add" onclick="addWork()">เพิ่มผลงาน</button>
  </div>
</section>

<section id="about">
  <div class="card">
    <div class="title">เกี่ยวกับฉัน</div>
    <p>
      <b>ชื่อ:</b> กฤษฎา ฉัตรกั้น<br>
      <b>ชั้น:</b> ม.4/3 เลขที่ 1<br>
      <b>โรงเรียน:</b> มัธยมนาคนาวาอุปถัมภ์<br>
      <b>ความสนใจ:</b> สาวสวย
    </p>
  </div>
</section>

<section id="skills">
  <div class="card">
    <div class="title">ทักษะ</div>
    <div class="skills">
      <span>ออกแบบ</span> <span>ตัดต่อ</span> <span>เขียนโค้ด</span> <span>สร้างสรรค์</span>
    </div>
  </div>
</section>

<section id="contact">
  <div class="card">
    <div class="title">ติดต่อฉัน</div>
    <p>อีเมล: krisada.cha@edu.bangkok.go.th</p>
    <form action="https://formspree.io/f/abcdwxyz" method="POST">
      <input type="text" name="social" placeholder="Facebook / IG" required>
      <input type="text" name="phone" placeholder="เบอร์โทร" required>
      <textarea name="message" placeholder="ข้อความถึงฉัน" required></textarea>
      <button class="btn-add" type="submit">ส่งข้อความ</button>
    </form>
  </div>
</section>

<footer>
  © 2026 Portfolio | กฤษฎา ฉัตรกั้น
</footer>

<script>
function addWork(){
  const title = document.getElementById('workTitle').value;
  const fileInput = document.getElementById('workImage');
  const file = fileInput.files[0];
  const link = document.getElementById('workLink').value;

  // เช็คแค่ชื่ออย่างเดียวพอ
  if(!title){
    alert("กรุณาใส่ชื่อผลงานด้วยครับ");
    return;
  }

  const gallery = document.getElementById('gallery');
  const div = document.createElement('div');
  div.className = 'work';

  // ถ้ามีการเลือกไฟล์ ให้ใช้ FileReader
  if(file){
    const reader = new FileReader();
    reader.onload = function(e){
      renderCard(div, e.target.result, title, link);
      gallery.appendChild(div);
    };
    reader.readAsDataURL(file);
  } else {
    // ถ้าไม่มีไฟล์ ให้ใช้รูป Placeholder สีเขียวเท่ๆ แทน
    const noImg = "https://via.placeholder.com/300x180/0f2e1f/2ecc71?text=No+Image";
    renderCard(div, noImg, title, link);
    gallery.appendChild(div);
  }

  // ล้างค่าหลังจากกดเพิ่ม
  document.getElementById('workTitle').value = '';
  fileInput.value = '';
  document.getElementById('workLink').value = '';
}

// ฟังก์ชันแยกสำหรับสร้างเนื้อหาในการ์ด
function renderCard(targetDiv, imgSrc, title, link){
  targetDiv.innerHTML = `
    <img src="${imgSrc}">
    <b style="display:block; margin-bottom:5px;">${title}</b>
    <a href="${link || '#'}" target="_blank" style="color:#2ecc71; text-decoration:none; font-size:14px;">${link ? '🔗 เปิดลิ้ง' : 'ไม่มีลิงก์'}</a><br>
    <button class="btn-delete" onclick="this.parentElement.remove()">ลบ</button>
  `;
}
</script>

</body>
</html>
