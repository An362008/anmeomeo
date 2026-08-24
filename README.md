
<!DOCTYPE html>

<html lang="vi">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Toán Đại Số 7 - Học, Tính toán & Bài tập</title>

<style>

*{box-sizing:border-box}

body{margin:0;font-family:Arial,Helvetica,sans-serif;background:linear-gradient(135deg,#6c63ff,#00c6ff,#7bed9f);background-size:300% 300%;animation:bg 12s ease infinite;color:#172033;min-height:100vh}

@keyframes bg{0%,100%{background-position:0 50%}50%{background-position:100% 50%}}

header{padding:34px 20px;text-align:center;color:white}

header h1{font-size:clamp(32px,6vw,58px);margin:0 0 8px;text-shadow:0 5px 15px #0005}

header p{font-size:18px;margin:0}

nav{position:sticky;top:0;z-index:20;background:#ffffffdd;backdrop-filter:blur(12px);box-shadow:0 5px 20px #0002;display:flex;justify-content:center;gap:10px;padding:12px;flex-wrap:wrap}

nav button,.btn{border:0;border-radius:14px;padding:12px 18px;font-weight:700;cursor:pointer;transition:.2s}

nav button{background:#eef1ff;color:#4b43c6}

nav button:hover,.btn:hover{transform:translateY(-3px);box-shadow:0 8px 18px #0002}

.container{max-width:1150px;margin:25px auto;padding:0 16px}

.page{display:none}.page.active{display:block}

.hero,.panel,.topic,.question,.score{background:#fffffff2;border-radius:24px;box-shadow:0 12px 35px #0002}

.hero{padding:35px;text-align:center}

.hero h2{font-size:34px;margin:0 0 12px;color:#5148d8}

.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;margin-top:25px}

.topic{padding:24px;cursor:pointer;transition:.25s;border:3px solid transparent}

.topic:hover{transform:translateY(-7px) rotate(.5deg);border-color:#7c72ff}

.topic .icon{font-size:45px}.topic h3{margin:10px 0 7px}.topic p{color:#586174}

.panel{padding:28px;margin-bottom:20px}

.panel h2{color:#5148d8;margin-top:0}

.subnav{display:flex;flex-wrap:wrap;gap:9px;margin-bottom:20px}

.subnav button{background:#f0f2ff;color:#4c45bb;border:2px solid #dfe2ff;border-radius:12px;padding:10px 13px;font-weight:700;cursor:pointer}

.lesson{display:none}.lesson.active{display:block}

.lesson h3{font-size:25px;color:#3f38a8}.formula{background:#f2f8ff;border-left:5px solid #00a8ff;padding:14px;border-radius:12px;font-size:20px;margin:12px 0}

.example{background:#f7fff4;border-left:5px solid #2ed573;padding:14px;border-radius:12px}

label{display:block;font-weight:700;margin-top:10px}input,select{width:100%;padding:12px;border:2px solid #dfe3ef;border-radius:12px;font-size:16px;margin-top:6px}

.btn{background:linear-gradient(135deg,#6258e8,#00a8ff);color:white;margin-top:14px}

.result{margin-top:15px;padding:15px;border-radius:14px;background:#ecfff5;border-left:5px solid #20bf6b;line-height:1.7}

.question{padding:20px;margin:15px 0;border-left:6px solid #6c63ff}

.question h3{margin-top:0}.options label{font-weight:400;background:#f7f8ff;padding:11px;border-radius:10px;margin:8px 0;cursor:pointer}.options label:hover{background:#e9ebff}

.topic-filter{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:15px}.topic-filter button{border:0;background:#eeeefd;padding:9px 13px;border-radius:12px;cursor:pointer;font-weight:700}

.quiz-head{display:flex;justify-content:space-between;gap:15px;align-items:center;flex-wrap:wrap;background:#fff;padding:16px;border-radius:18px;margin-bottom:15px}

.badge{padding:9px 13px;background:#fff2a8;border-radius:12px;font-weight:800}

#quizArea{display:none}

#quizArea.show{display:block}

.progress{height:12px;background:#e8eaf2;border-radius:20px;overflow:hidden}.progress span{display:block;height:100%;background:linear-gradient(90deg,#ff6b6b,#ffd32a,#20bf6b);width:0;transition:.3s}

.score{text-align:center;padding:30px;display:none}.score.show{display:block}

.score .big{font-size:52px;font-weight:900;color:#5148d8}

footer{text-align:center;color:white;padding:25px}

.small{color:#667085;font-size:14px}

@media(max-width:650px){.hero,.panel{padding:20px}.quiz-head{display:block}.quiz-head>*{margin:5px 0}}

</style>

</head>

<body>

<header>

  <h1>📚 TOÁN ĐẠI SỐ 7</h1>

  <p>Học lý thuyết • Tính toán • Luyện bài tập • Tính điểm tự động</p>

</header>



<nav>

  <button onclick="showPage('home')">🏠 Trang chủ</button>

  <button onclick="showPage('theory')">📖 Lý thuyết</button>

  <button onclick="showPage('calc')">🧮 Tính toán</button>

  <button onclick="showPage('practice')">📝 Bài tập</button>

</nav>



<main class="container">



<section id="home" class="page active">

  <div class="hero">

    <h2>🌟 Chào mừng đến với Toán Đại Số 7!</h2>

    <p>Chọn một khu vực để bắt đầu học.</p>

    <div class="cards">

      <div class="topic" onclick="showPage('theory')"><div class="icon">📖</div><h3>LÝ THUYẾT</h3><p>Chia thành từng chuyên đề, học theo từng phần.</p></div>

      <div class="topic" onclick="showPage('calc')"><div class="icon">🧮</div><h3>TÍNH TOÁN</h3><p>Mỗi chuyên đề có công cụ tính riêng.</p></div>

      <div class="topic" onclick="showPage('practice')"><div class="icon">📝</div><h3>BÀI TẬP</h3><p>Nhiều phần, nhiều câu hỏi và chấm điểm tự động.</p></div>

    </div>

  </div>

</section>



<section id="theory" class="page">

<div class="panel">

<h2>📖 Lý thuyết Toán 7</h2>

<div class="subnav">

<button onclick="lesson('lt1')">🔢 Số hữu tỉ</button>

<button onclick="lesson('lt2')">⚡ Lũy thừa</button>

<button onclick="lesson('lt3')">📐 Tỉ lệ thức</button>

<button onclick="lesson('lt4')">📈 Tỉ lệ thuận</button>

<button onclick="lesson('lt5')">📉 Tỉ lệ nghịch</button>

<button onclick="lesson('lt6')">🧮 Biểu thức</button>

<button onclick="lesson('lt7')">✏️ Đơn thức</button>

<button onclick="lesson('lt8')">📊 Đa thức</button>

<button onclick="lesson('lt9')">🎯 Nghiệm đa thức</button>

<button onclick="lesson('lt10')">📋 Thống kê</button>

</div>



<div id="lt1" class="lesson active"><h3>🔢 Số hữu tỉ</h3><p>Số hữu tỉ là số viết được dưới dạng a/b, trong đó a,b là số nguyên và b khác 0.</p><div class="formula">a/b + c/d = (ad + bc)/bd</div><div class="formula">a/b × c/d = ac/bd</div><div class="example">Ví dụ: 1/2 + 1/3 = 5/6.</div></div>

<div id="lt2" class="lesson"><h3>⚡ Lũy thừa</h3><p>Lũy thừa biểu thị phép nhân một số với chính nó nhiều lần.</p><div class="formula">aᵐ × aⁿ = aᵐ⁺ⁿ</div><div class="formula">aᵐ : aⁿ = aᵐ⁻ⁿ (a ≠ 0)</div></div>

<div id="lt3" class="lesson"><h3>📐 Tỉ lệ thức</h3><p>Tỉ lệ thức là một đẳng thức của hai tỉ số.</p><div class="formula">a/b = c/d ⇒ ad = bc</div><div class="example">Có thể dùng tính chất này để tìm số chưa biết.</div></div>

<div id="lt4" class="lesson"><h3>📈 Đại lượng tỉ lệ thuận</h3><p>Nếu y = kx thì y tỉ lệ thuận với x theo hệ số k.</p><div class="formula">y/x = k</div></div>

<div id="lt5" class="lesson"><h3>📉 Đại lượng tỉ lệ nghịch</h3><p>Nếu y = a/x với a khác 0 thì y tỉ lệ nghịch với x.</p><div class="formula">x × y = a</div></div>

<div id="lt6" class="lesson"><h3>🧮 Biểu thức đại số</h3><p>Biểu thức đại số gồm số, biến và các phép toán.</p><div class="example">Ví dụ: A = 2x² + 3x - 5.</div></div>

<div id="lt7" class="lesson"><h3>✏️ Đơn thức</h3><p>Đơn thức là biểu thức đại số chỉ gồm một số, một biến hoặc tích của số và biến.</p><div class="example">Ví dụ: 3x²y là một đơn thức.</div></div>

<div id="lt8" class="lesson"><h3>📊 Đa thức</h3><p>Đa thức là tổng của những đơn thức.</p><div class="example">Ví dụ: P(x) = 2x² + 3x - 5.</div></div>

<div id="lt9" class="lesson"><h3>🎯 Nghiệm của đa thức</h3><p>Số a là nghiệm của P(x) nếu P(a) = 0.</p><div class="formula">P(a) = 0 ⇒ a là nghiệm của P(x)</div></div>

<div id="lt10" class="lesson"><h3>📋 Thống kê</h3><p>Dữ liệu có thể được thu thập, phân loại và biểu diễn bằng bảng hoặc biểu đồ. Trung bình cộng bằng tổng các giá trị chia cho số giá trị.</p></div>

</div>

</section>



<section id="calc" class="page">

<div class="panel">

<h2>🧮 Tính toán theo từng phần</h2>

<div class="subnav">

<button onclick="calc('c1')">➗ Phân số</button>

<button onclick="calc('c2')">⚡ Lũy thừa</button>

<button onclick="calc('c3')">📐 Tỉ lệ thức</button>

<button onclick="calc('c4')">📈 Tỉ lệ thuận</button>

<button onclick="calc('c5')">📉 Tỉ lệ nghịch</button>

<button onclick="calc('c6')">🧮 Biểu thức</button>

<button onclick="calc('c7')">✏️ Đơn thức</button>

<button onclick="calc('c8')">📊 Đa thức</button>

<button onclick="calc('c9')">🎯 Phương trình</button>

<button onclick="calc('c10')">📋 Thống kê</button>

</div>



<div id="c1" class="lesson active"><h3>➗ Tính phân số</h3><input id="a" type="number" placeholder="Tử số a"><input id="b" type="number" placeholder="Mẫu số b"><input id="c" type="number" placeholder="Tử số c"><input id="d" type="number" placeholder="Mẫu số d"><button class="btn" onclick="fraction()">✨ Tính</button><div id="r1" class="result"></div></div>

<div id="c2" class="lesson"><h3>⚡ Tính lũy thừa</h3><input id="base" type="number" placeholder="Cơ số a"><input id="exp" type="number" placeholder="Số mũ n"><button class="btn" onclick="power()">✨ Tính</button><div id="r2" class="result"></div></div>

<div id="c3" class="lesson"><h3>📐 Tìm x trong a/b = x/d</h3><input id="ta" type="number" placeholder="a"><input id="tb" type="number" placeholder="b"><input id="td" type="number" placeholder="d"><button class="btn" onclick="ratio()">✨ Tìm x</button><div id="r3" class="result"></div></div>

<div id="c4" class="lesson"><h3>📈 Tỉ lệ thuận</h3><input id="tx1" type="number" placeholder="x₁"><input id="ty1" type="number" placeholder="y₁"><input id="tx2" type="number" placeholder="x₂"><button class="btn" onclick="direct()">✨ Tìm y₂</button><div id="r4" class="result"></div></div>

<div id="c5" class="lesson"><h3>📉 Tỉ lệ nghịch</h3><input id="ix1" type="number" placeholder="x₁"><input id="iy1" type="number" placeholder="y₁"><input id="ix2" type="number" placeholder="x₂"><button class="btn" onclick="inverse()">✨ Tìm y₂</button><div id="r5" class="result"></div></div>

<div id="c6" class="lesson"><h3>🧮 A = 2x² + 3x - 5</h3><input id="bx" type="number" placeholder="Nhập x"><button class="btn" onclick="expr()">✨ Tính A</button><div id="r6" class="result"></div></div>

<div id="c7" class="lesson"><h3>✏️ A = a × xⁿ</h3><input id="da" type="number" placeholder="a"><input id="dx" type="number" placeholder="x"><input id="dn" type="number" placeholder="n"><button class="btn" onclick="mono()">✨ Tính A</button><div id="r7" class="result"></div></div>

<div id="c8" class="lesson"><h3>📊 P(x) = ax² + bx + c</h3><input id="pa" type="number" placeholder="a"><input id="pb" type="number" placeholder="b"><input id="pc" type="number" placeholder="c"><input id="px" type="number" placeholder="x"><button class="btn" onclick="poly()">✨ Tính P(x)</button><div id="r8" class="result"></div></div>

<div id="c9" class="lesson"><h3>🎯 Giải ax + b = 0</h3><input id="qa" type="number" placeholder="a"><input id="qb" type="number" placeholder="b"><button class="btn" onclick="equation()">✨ Giải</button><div id="r9" class="result"></div></div>

<div id="c10" class="lesson"><h3>📋 Thống kê</h3><input id="nums" placeholder="Ví dụ: 5, 7, 8, 10, 12"><button class="btn" onclick="stats()">✨ Thống kê</button><div id="r10" class="result"></div></div>

</div>

</section>



<section id="practice" class="page">

<div class="panel">

<h2>📝 Bài tập nhiều phần - tính điểm tự động</h2>

<p class="small">Mỗi đề có nhiều chuyên đề. Mỗi câu đúng được 1 điểm. Điểm cuối = số câu đúng / tổng số câu × 10.</p>

<div class="topic-filter">

<button onclick="startQuiz('all')">🌟 Tổng hợp</button>

<button onclick="startQuiz('fraction')">➗ Số hữu tỉ</button>

<button onclick="startQuiz('power')">⚡ Lũy thừa</button>

<button onclick="startQuiz('ratio')">📐 Tỉ lệ thức</button>

<button onclick="startQuiz('algebra')">🧮 Đại số</button>

<button onclick="startQuiz('stats')">📋 Thống kê</button>

</div>

<div id="quizArea">

<div class="quiz-head"><div><b id="quizTitle">Đề bài</b><br><span id="count"></span></div><div class="badge">🏆 Điểm: <span id="liveScore">0</span></div></div>

<div class="progress"><span id="bar"></span></div>

<form id="quizForm"></form>

<button class="btn" onclick="submitQuiz()">🎯 NỘP BÀI & TÍNH ĐIỂM</button>

<div id="scoreBox" class="score"></div>

</div>

</div>

</section>



</main>

<footer>🎓 Toán Đại Số 7 • Học vui - Luyện giỏi • Chạy trực tiếp trên trình duyệt</footer>



<script>

function showPage(id){document.querySelectorAll('.page').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active');scrollTo({top:0,behavior:'smooth'})}

function lesson(id){document.querySelectorAll('#theory .lesson').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active')}

function calc(id){document.querySelectorAll('#calc .lesson').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active')}

const n=id=>Number(document.getElementById(id).value);

function fraction(){let a=n('a'),b=n('b'),c=n('c'),d=n('d');let r=document.getElementById('r1');if(!b||!d){r.innerHTML='⚠️ Mẫu số phải khác 0';return}r.innerHTML=`➕ Tổng: ${(a*d+b*c)/(b*d)}<br>➖ Hiệu: ${(a*d-b*c)/(b*d)}<br>✖️ Tích: ${(a*c)/(b*d)}<br>➗ Thương: ${c?((a*d)/(b*c)):'Không xác định'}`}

function power(){document.getElementById('r2').innerHTML=`🎯 Kết quả: <b>${Math.pow(n('base'),n('exp'))}</b>`}

function ratio(){let a=n('ta'),b=n('tb'),d=n('td');document.getElementById('r3').innerHTML=b?`🎯 x = <b>${a*d/b}</b>`:'⚠️ b phải khác 0'}

function direct(){let x1=n('tx1'),y1=n('ty1'),x2=n('tx2');document.getElementById('r4').innerHTML=x1?`🎯 y₂ = <b>${y1*x2/x1}</b>`:'⚠️ x₁ phải khác 0'}

function inverse(){let x1=n('ix1'),y1=n('iy1'),x2=n('ix2');document.getElementById('r5').innerHTML=x2?`🎯 y₂ = <b>${x1*y1/x2}</b>`:'⚠️ x₂ phải khác 0'}

function expr(){let x=n('bx');document.getElementById('r6').innerHTML=`🎯 A = <b>${2*x*x+3*x-5}</b>`}

function mono(){document.getElementById('r7').innerHTML=`🎯 A = <b>${n('da')*Math.pow(n('dx'),n('dn'))}</b>`}

function poly(){let a=n('pa'),b=n('pb'),c=n('pc'),x=n('px');document.getElementById('r8').innerHTML=`🎯 P(x) = <b>${a*x*x+b*x+c}</b>`}

function equation(){let a=n('qa'),b=n('qb'),r=document.getElementById('r9');if(a===0)r.innerHTML=b===0?'♾️ Vô số nghiệm':'❌ Vô nghiệm';else r.innerHTML=`🎯 x = <b>${-b/a}</b>`}

function stats(){let a=document.getElementById('nums').value.split(',').map(Number).filter(x=>!isNaN(x));let r=document.getElementById('r10');if(!a.length){r.innerHTML='⚠️ Chưa có dữ liệu';return}let s=a.reduce((x,y)=>x+y,0);r.innerHTML=`📊 Số lượng: ${a.length}<br>➕ Tổng: ${s}<br>📈 Trung bình: ${s/a.length}<br>🔺 Lớn nhất: ${Math.max(...a)}<br>🔻 Nhỏ nhất: ${Math.min(...a)}`}



const Q=[

{t:'fraction',q:'Tính 1/2 + 1/3 bằng bao nhiêu?',o:['5/6','2/5','1/6','3/5'],a:0},

{t:'fraction',q:'Tính 3/4 - 1/4 bằng bao nhiêu?',o:['1/2','1/4','2/3','3/8'],a:0},

{t:'fraction',q:'Tính 2/3 × 3/4 bằng bao nhiêu?',o:['1/2','2/7','5/12','3/8'],a:0},

{t:'power',q:'2³ bằng bao nhiêu?',o:['6','8','9','12'],a:1},

{t:'power',q:'3² × 3³ bằng bao nhiêu?',o:['3⁵','3⁶','9⁵','6⁵'],a:0},

{t:'power',q:'5⁰ bằng bao nhiêu?',o:['0','1','5','10'],a:1},

{t:'ratio',q:'Nếu a/b = c/d thì đẳng thức nào đúng?',o:['ab = cd','ad = bc','a+c = b+d','a/b = d/c'],a:1},

{t:'ratio',q:'2/3 = x/12. Giá trị x là?',o:['6','8','9','10'],a:1},

{t:'ratio',q:'3/5 = 12/x. Giá trị x là?',o:['15','18','20','25'],a:2},

{t:'algebra',q:'Với x = 2, A = 2x² + 3x - 5 bằng?',o:['5','7','9','11'],a:1},

{t:'algebra',q:'Đơn thức nào sau đây?',o:['2x²','x+2','x²-1','2/x'],a:0},

{t:'algebra',q:'Nếu P(x)=x-3 thì nghiệm của P là?',o:['-3','0','1','3'],a:3},

{t:'stats',q:'Trung bình cộng của 4, 6, 8 là?',o:['5','6','7','8'],a:1},

{t:'stats',q:'Số lớn nhất trong 3, 9, 5, 7 là?',o:['3','5','7','9'],a:3},

{t:'stats',q:'Dãy 2, 4, 6, 8 có bao nhiêu giá trị?',o:['2','3','4','5'],a:2}

];

let current=[],submitted=false;

function startQuiz(type){

 current=type==='all'?[...Q]:Q.filter(x=>x.t===type);

 submitted=false;

 document.getElementById('quizArea').classList.add('show');

 document.getElementById('scoreBox').classList.remove('show');

 document.getElementById('quizTitle').textContent=type==='all'?'🌟 Đề tổng hợp Toán Đại Số 7':'📝 Bài tập: '+({fraction:'Số hữu tỉ',power:'Lũy thừa',ratio:'Tỉ lệ thức',algebra:'Đại số',stats:'Thống kê'}[type]);

 document.getElementById('count').textContent=current.length+' câu hỏi';

 document.getElementById('liveScore').textContent='0';

 let f=document.getElementById('quizForm');f.innerHTML='';

 current.forEach((x,i)=>{let d=document.createElement('div');d.className='question';d.innerHTML=`<h3>Câu ${i+1}: ${x.q}</h3><div class="options">${x.o.map((o,j)=>`<label><input type="radio" name="q${i}" value="${j}"> ${String.fromCharCode(65+j)}. ${o}</label>`).join('')}</div>`;f.appendChild(d)});

 document.getElementById('bar').style.width='0%';

 window.scrollTo({top:document.getElementById('quizArea').offsetTop-80,behavior:'smooth'});

}

function submitQuiz(){

 if(submitted)return;

 let score=0,answered=0;

 current.forEach((x,i)=>{let el=document.querySelector(`input[name="q${i}"]:checked`);if(el){answered++;if(Number(el.value)===x.a)score++}});

 let point=(score/current.length*10);

 let box=document.getElementById('scoreBox');

 box.classList.add('show');

 box.innerHTML=`<div class="big">${point.toFixed(1)}/10</div><h2>🎉 Hoàn thành bài!</h2><p><b>${score}/${current.length}</b> câu đúng • Đã trả lời ${answered}/${current.length} câu</p><p>${point>=8?'🌟 Rất tốt!':point>=5?'👍 Cố gắng thêm nhé!':'💪 Hãy xem lại lý thuyết và làm lại!'}</p>`;

 document.getElementById('liveScore').textContent=score;

 document.getElementById('bar').style.width=(score/current.length*100)+'%';

 submitted=true;

}

</script>

</body>

</html>


HTML
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Toán Đại Số 7 - Học, Tính toán & Bài tập</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,Helvetica,sans-serif;background:linear-gradient(135deg,#6c63ff,#00c6ff,#7bed9f);background-size:300% 300%;animation:bg 12s ease infinite;color:#172033;min-height:100vh}
@keyframes bg{0%,100%{background-position:0 50%}50%{background-position:100% 50%}}
header{padding:34px 20px;text-align:center;color:white}
header h1{font-size:clamp(32px,6vw,58px);margin:0 0 8px;text-shadow:0 5px 15px #0005}
header p{font-size:18px;margin:0}
nav{position:sticky;top:0;z-index:20;background:#ffffffdd;backdrop-filter:blur(12px);box-shadow:0 5px 20px #0002;display:flex;justify-content:center;gap:10px;padding:12px;flex-wrap:wrap}
nav button,.btn{border:0;border-radius:14px;padding:12px 18px;font-weight:700;cursor:pointer;transition:.2s}
nav button{background:#eef1ff;color:#4b43c6}
nav button:hover,.btn:hover{transform:translateY(-3px);box-shadow:0 8px 18px #0002}
.container{max-width:1150px;margin:25px auto;padding:0 16px}
.page{display:none}.page.active{display:block}
.hero,.panel,.topic,.question,.score{background:#fffffff2;border-radius:24px;box-shadow:0 12px 35px #0002}
.hero{padding:35px;text-align:center}
.hero h2{font-size:34px;margin:0 0 12px;color:#5148d8}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;margin-top:25px}
.topic{padding:24px;cursor:pointer;transition:.25s;border:3px solid transparent}
.topic:hover{transform:translateY(-7px) rotate(.5deg);border-color:#7c72ff}
.topic .icon{font-size:45px}.topic h3{margin:10px 0 7px}.topic p{color:#586174}
.panel{padding:28px;margin-bottom:20px}
.panel h2{color:#5148d8;margin-top:0}
.subnav{display:flex;flex-wrap:wrap;gap:9px;margin-bottom:20px}
.subnav button{background:#f0f2ff;color:#4c45bb;border:2px solid #dfe2ff;border-radius:12px;padding:10px 13px;font-weight:700;cursor:pointer}
.lesson{display:none}.lesson.active{display:block}
.lesson h3{font-size:25px;color:#3f38a8}.formula{background:#f2f8ff;border-left:5px solid #00a8ff;padding:14px;border-radius:12px;font-size:20px;margin:12px 0}
.example{background:#f7fff4;border-left:5px solid #2ed573;padding:14px;border-radius:12px}
label{display:block;font-weight:700;margin-top:10px}input,select{width:100%;padding:12px;border:2px solid #dfe3ef;border-radius:12px;font-size:16px;margin-top:6px}
.btn{background:linear-gradient(135deg,#6258e8,#00a8ff);color:white;margin-top:14px}
.result{margin-top:15px;padding:15px;border-radius:14px;background:#ecfff5;border-left:5px solid #20bf6b;line-height:1.7}
.question{padding:20px;margin:15px 0;border-left:6px solid #6c63ff;transition:.3s}
.question.correct{border-left-color:#20bf6b;background:#f0fff4}
.question.incorrect{border-left-color:#ff4757;background:#fff0f0}
.question h3{margin-top:0}.options label{font-weight:400;background:#f7f8ff;padding:11px;border-radius:10px;margin:8px 0;cursor:pointer;display:block}.options label:hover{background:#e9ebff}
.topic-filter{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:15px}.topic-filter button{border:0;background:#eeeefd;padding:9px 13px;border-radius:12px;cursor:pointer;font-weight:700}
.quiz-head{display:flex;justify-content:space-between;gap:15px;align-items:center;flex-wrap:wrap;background:#fff;padding:16px;border-radius:18px;margin-bottom:15px}
.badge{padding:9px 13px;background:#fff2a8;border-radius:12px;font-weight:800}
#quizArea{display:none}
#quizArea.show{display:block}
.progress{height:12px;background:#e8eaf2;border-radius:20px;overflow:hidden}.progress span{display:block;height:100%;background:linear-gradient(90deg,#ff6b6b,#ffd32a,#20bf6b);width:0;transition:.3s}
.score{text-align:center;padding:30px;display:none}.score.show{display:block}
.score .big{font-size:52px;font-weight:900;color:#5148d8}
footer{text-align:center;color:white;padding:25px}
.small{color:#667085;font-size:14px}
@media(max-width:650px){.hero,.panel{padding:20px}.quiz-head{display:block}.quiz-head>*{margin:5px 0}}
</style>
</head>
<body>
<header>
  <h1>📚 TOÁN ĐẠI SỐ 7</h1>
  <p>Học lý thuyết • Tính toán • Luyện bài tập • Tính điểm tự động</p>
</header>

<nav>
  <button onclick="showPage('home')">🏠 Trang chủ</button>
  <button onclick="showPage('theory')">📖 Lý thuyết</button>
  <button onclick="showPage('calc')">🧮 Tính toán</button>
  <button onclick="showPage('practice')">📝 Bài tập</button>
</nav>

<main class="container">

<section id="home" class="page active">
  <div class="hero">
    <h2>🌟 Chào mừng đến với Toán Đại Số 7!</h2>
    <p>Chọn một khu vực để bắt đầu học.</p>
    <div class="cards">
      <div class="topic" onclick="showPage('theory')"><div class="icon">📖</div><h3>LÝ THUYẾT</h3><p>Chia thành từng chuyên đề, học theo từng phần.</p></div>
      <div class="topic" onclick="showPage('calc')"><div class="icon">🧮</div><h3>TÍNH TOÁN</h3><p>Mỗi chuyên đề có công cụ tính riêng.</p></div>
      <div class="topic" onclick="showPage('practice')"><div class="icon">📝</div><h3>BÀI TẬP</h3><p>Nhiều phần, nhiều câu hỏi và chấm điểm tự động.</p></div>
    </div>
  </div>
</section>

<section id="theory" class="page">
<div class="panel">
<h2>📖 Lý thuyết Toán 7</h2>
<div class="subnav">
<button onclick="lesson('lt1')">🔢 Số hữu tỉ</button>
<button onclick="lesson('lt2')">⚡ Lũy thừa</button>
<button onclick="lesson('lt3')">📐 Tỉ lệ thức</button>
<button onclick="lesson('lt4')">📈 Tỉ lệ thuận</button>
<button onclick="lesson('lt5')">📉 Tỉ lệ nghịch</button>
<button onclick="lesson('lt6')">🧮 Biểu thức</button>
<button onclick="lesson('lt7')">✏️ Đơn thức</button>
<button onclick="lesson('lt8')">📊 Đa thức</button>
<button onclick="lesson('lt9')">🎯 Nghiệm đa thức</button>
<button onclick="lesson('lt10')">📋 Thống kê</button>
</div>

<div id="lt1" class="lesson active"><h3>🔢 Số hữu tỉ</h3><p>Số hữu tỉ là số viết được dưới dạng a/b, trong đó a,b là số nguyên và b khác 0.</p><div class="formula">a/b + c/d = (ad + bc)/bd</div><div class="formula">a/b × c/d = ac/bd</div><div class="example">Ví dụ: 1/2 + 1/3 = 5/6.</div></div>
<div id="lt2" class="lesson"><h3>⚡ Lũy thừa</h3><p>Lũy thừa biểu thị phép nhân một số với chính nó nhiều lần.</p><div class="formula">aᵐ × aⁿ = aᵐ⁺ⁿ</div><div class="formula">aᵐ : aⁿ = aᵐ⁻ⁿ (a ≠ 0)</div></div>
<div id="lt3" class="lesson"><h3>📐 Tỉ lệ thức</h3><p>Tỉ lệ thức là một đẳng thức của hai tỉ số.</p><div class="formula">a/b = c/d ⇒ ad = bc</div><div class="example">Có thể dùng tính chất này để tìm số chưa biết.</div></div>
<div id="lt4" class="lesson"><h3>📈 Đại lượng tỉ lệ thuận</h3><p>Nếu y = kx thì y tỉ lệ thuận với x theo hệ số k.</p><div class="formula">y/x = k</div></div>
<div id="lt5" class="lesson"><h3>📉 Đại lượng tỉ lệ nghịch</h3><p>Nếu y = a/x với a khác 0 thì y tỉ lệ nghịch với x.</p><div class="formula">x × y = a</div></div>
<div id="lt6" class="lesson"><h3>🧮 Biểu thức đại số</h3><p>Biểu thức đại số gồm số, biến và các phép toán.</p><div class="example">Ví dụ: A = 2x² + 3x - 5.</div></div>
<div id="lt7" class="lesson"><h3>✏️ Đơn thức</h3><p>Đơn thức là biểu thức đại số chỉ gồm một số, một biến hoặc tích của số và biến.</p><div class="example">Ví dụ: 3x²y là một đơn thức.</div></div>
<div id="lt8" class="lesson"><h3>📊 Đa thức</h3><p>Đa thức là tổng của những đơn thức.</p><div class="example">Ví dụ: P(x) = 2x² + 3x - 5.</div></div>
<div id="lt9" class="lesson"><h3>🎯 Nghiệm của đa thức</h3><p>Số a là nghiệm của P(x) nếu P(a) = 0.</p><div class="formula">P(a) = 0 ⇒ a là nghiệm của P(x)</div></div>
<div id="lt10" class="lesson"><h3>📋 Thống kê</h3><p>Dữ liệu có thể được thu thập, phân loại và biểu diễn bằng bảng hoặc biểu đồ. Trung bình cộng bằng tổng các giá trị chia cho số giá trị.</p></div>
</div>
</section>

<section id="calc" class="page">
<div class="panel">
<h2>🧮 Tính toán theo từng phần</h2>
<div class="subnav">
<button onclick="calc('c1')">➗ Phân số</button>
<button onclick="calc('c2')">⚡ Lũy thừa</button>
<button onclick="calc('c3')">📐 Tỉ lệ thức</button>
<button onclick="calc('c4')">📈 Tỉ lệ thuận</button>
<button onclick="calc('c5')">📉 Tỉ lệ nghịch</button>
<button onclick="calc('c6')">🧮 Biểu thức</button>
<button onclick="calc('c7')">✏️ Đơn thức</button>
<button onclick="calc('c8')">📊 Đa thức</button>
<button onclick="calc('c9')">🎯 Phương trình</button>
<button onclick="calc('c10')">📋 Thống kê</button>
</div>

<div id="c1" class="lesson active"><h3>➗ Tính phân số</h3><input id="a" type="number" placeholder="Tử số a"><input id="b" type="number" placeholder="Mẫu số b"><input id="c" type="number" placeholder="Tử số c"><input id="d" type="number" placeholder="Mẫu số d"><button class="btn" onclick="fraction()">✨ Tính</button><div id="r1" class="result"></div></div>
<div id="c2" class="lesson"><h3>⚡ Tính lũy thừa</h3><input id="base" type="number" placeholder="Cơ số a"><input id="exp" type="number" placeholder="Số mũ n"><button class="btn" onclick="power()">✨ Tính</button><div id="r2" class="result"></div></div>
<div id="c3" class="lesson"><h3>📐 Tìm x trong a/b = x/d</h3><input id="ta" type="number" placeholder="a"><input id="tb" type="number" placeholder="b"><input id="td" type="number" placeholder="d"><button class="btn" onclick="ratio()">✨ Tìm x</button><div id="r3" class="result"></div></div>
<div id="c4" class="lesson"><h3>📈 Tỉ lệ thuận</h3><input id="tx1" type="number" placeholder="x₁"><input id="ty1" type="number" placeholder="y₁"><input id="tx2" type="number" placeholder="x₂"><button class="btn" onclick="direct()">✨ Tìm y₂</button><div id="r4" class="result"></div></div>
<div id="c5" class="lesson"><h3>📉 Tỉ lệ nghịch</h3><input id="ix1" type="number" placeholder="x₁"><input id="iy1" type="number" placeholder="y₁"><input id="ix2" type="number" placeholder="x₂"><button class="btn" onclick="inverse()">✨ Tìm y₂</button><div id="r5" class="result"></div></div>
<div id="c6" class="lesson"><h3>🧮 A = 2x² + 3x - 5</h3><input id="bx" type="number" placeholder="Nhập x"><button class="btn" onclick="expr()">✨ Tính A</button><div id="r6" class="result"></div></div>
<div id="c7" class="lesson"><h3>✏️ A = a × xⁿ</h3><input id="da" type="number" placeholder="a"><input id="dx" type="number" placeholder="x"><input id="dn" type="number" placeholder="n"><button class="btn" onclick="mono()">✨ Tính A</button><div id="r7" class="result"></div></div>
<div id="c8" class="lesson"><h3>📊 P(x) = ax² + bx + c</h3><input id="pa" type="number" placeholder="a"><input id="pb" type="number" placeholder="b"><input id="pc" type="number" placeholder="c"><input id="px" type="number" placeholder="x"><button class="btn" onclick="poly()">✨ Tính P(x)</button><div id="r8" class="result"></div></div>
<div id="c9" class="lesson"><h3>🎯 Giải ax + b = 0</h3><input id="qa" type="number" placeholder="a"><input id="qb" type="number" placeholder="b"><button class="btn" onclick="equation()">✨ Giải</button><div id="r9" class="result"></div></div>
<div id="c10" class="lesson"><h3>📋 Thống kê</h3><input id="nums" placeholder="Ví dụ: 5, 7, 8, 10, 12"><button class="btn" onclick="stats()">✨ Thống kê</button><div id="r10" class="result"></div></div>
</div>
</section>

<section id="practice" class="page">
<div class="panel">
<h2>📝 Bài tập nhiều phần - tính điểm tự động</h2>
<p class="small">Mỗi đề có nhiều chuyên đề. Mỗi câu đúng được 1 điểm. Điểm cuối = số câu đúng / tổng số câu × 10.</p>
<div class="topic-filter">
<button onclick="startQuiz('all')">🌟 Tổng hợp</button>
<button onclick="startQuiz('fraction')">➗ Số hữu tỉ</button>
<button onclick="startQuiz('power')">⚡ Lũy thừa</button>
<button onclick="startQuiz('ratio')">📐 Tỉ lệ thức</button>
<button onclick="startQuiz('algebra')">🧮 Đại số</button>
<button onclick="startQuiz('stats')">📋 Thống kê</button>
</div>
<div id="quizArea">
<div class="quiz-head"><div><b id="quizTitle">Đề bài</b><br><span id="count"></span></div><div class="badge">🏆 Điểm: <span id="liveScore">0</span></div></div>
<div class="progress"><span id="bar"></span></div>
<form id="quizForm"></form>
<button class="btn" onclick="submitQuiz()">🎯 NỘP BÀI & TÍNH ĐIỂM</button>
<div id="scoreBox" class="score"></div>
</div>
</div>
</section>

</main>
<footer>🎓 Toán Đại Số 7 • Học vui - Luyện giỏi • Chạy trực tiếp trên trình duyệt</footer>

<script>
function showPage(id){document.querySelectorAll('.page').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active');scrollTo({top:0,behavior:'smooth'})}
function lesson(id){document.querySelectorAll('#theory .lesson').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active')}
function calc(id){document.querySelectorAll('#calc .lesson').forEach(x=>x.classList.remove('active'));document.getElementById(id).classList.add('active')}
const n=id=>Number(document.getElementById(id).value);

function fraction(){
  let a=n('a'),b=n('b'),c=n('c'),d=n('d');
  let r=document.getElementById('r1');
  if(!b||!d){r.innerHTML='⚠️ Mẫu số phải khác 0';return}
  let divRes = (c !== 0) ? ((a*d)/(b*c)).toFixed(2) : 'Không xác định (tử số c = 0)';
  r.innerHTML=`➕ Tổng: ${((a*d+b*c)/(b*d)).toFixed(2)}<br>➖ Hiệu: ${((a*d-b*c)/(b*d)).toFixed(2)}<br>✖️ Tích: ${((a*c)/(b*d)).toFixed(2)}<br>➗ Thương: ${divRes}`;
}

function power(){document.getElementById('r2').innerHTML=`🎯 Kết quả: <b>${Math.pow(n('base'),n('exp'))}</b>`}
function ratio(){let a=n('ta'),b=n('tb'),d=n('td');document.getElementById('r3').innerHTML=b?`🎯 x = <b>${(a*d/b).toFixed(2)}</b>`:'⚠️ b phải khác 0'}
function direct(){let x1=n('tx1'),y1=n('ty1'),x2=n('tx2');document.getElementById('r4').innerHTML=x1?`🎯 y₂ = <b>${(y1*x2/x1).toFixed(2)}</b>`:'⚠️ x₁ phải khác 0'}
function inverse(){let x1=n('ix1'),y1=n('iy1'),x2=n('ix2');document.getElementById('r5').innerHTML=x2?`🎯 y₂ = <b>${(x1*y1/x2).toFixed(2)}</b>`:'⚠️ x₂ phải khác 0'}
function expr(){let x=n('bx');document.getElementById('r6').innerHTML=`🎯 A = <b>${2*x*x+3*x-5}</b>`}
function mono(){document.getElementById('r7').innerHTML=`🎯 A = <b>${n('da')*Math.pow(n('dx'),n('dn'))}</b>`}
function poly(){let a=n('pa'),b=n('pb'),c=n('pc'),x=n('px');document.getElementById('r8').innerHTML=`🎯 P(x) = <b>${a*x*x+b*x+c}</b>`}
function equation(){let a=n('qa'),b=n('qb'),r=document.getElementById('r9');if(a===0)r.innerHTML=b===0?'♾️ Vô số nghiệm':'❌ Vô nghiệm';else r.innerHTML=`🎯 x = <b>${-b/a}</b>`}

function stats(){
  let val=document.getElementById('nums').value;
  let a=val.split(',').map(x=>x.trim()).filter(x=>x!=='').map(Number).filter(x=>!isNaN(x));
  let r=document.getElementById('r10');
  if(!a.length){r.innerHTML='⚠️ Chưa có dữ liệu hợp lệ';return}
  let s=a.reduce((x,y)=>x+y,0);
  r.innerHTML=`📊 Số lượng: ${a.length}<br>➕ Tổng: ${s}<br>📈 Trung bình: ${(s/a.length).toFixed(2)}<br>🔺 Lớn nhất: ${Math.max(...a)}<br>🔻 Nhỏ nhất: ${Math.min(...a)}`;
}

const Q=[
{t:'fraction',q:'Tính 1/2 + 1/3 bằng bao nhiêu?',o:['5/6','2/5','1/6','3/5'],a:0},
{t:'fraction',q:'Tính 3/4 - 1/4 bằng bao nhiêu?',o:['1/2','1/4','2/3','3/8'],a:0},
{t:'fraction',q:'Tính 2/3 × 3/4 bằng bao nhiêu?',o:['1/2','2/7','5/12','3/8'],a:0},
{t:'power',q:'2³ bằng bao nhiêu?',o:['6','8','9','12'],a:1},
{t:'power',q:'3² × 3³ bằng bao nhiêu?',o:['3⁵','3⁶','9⁵','6⁵'],a:0},
{t:'power',q:'5⁰ bằng bao nhiêu?',o:['0','1','5','10'],a:1},
{t:'ratio',q:'Nếu a/b = c/d thì đẳng thức nào đúng?',o:['ab = cd','ad = bc','a+c = b+d','a/b = d/c'],a:1},
{t:'ratio',q:'2/3 = x/12. Giá trị x là?',o:['6','8','9','10'],a:1},
{t:'ratio',q:'3/5 = 12/x. Giá trị x là?',o:['15','18','20','25'],a:2},
{t:'algebra',q:'Với x = 2, A = 2x² + 3x - 5 bằng?',o:['5','9','7','11'],a:1},
{t:'algebra',q:'Đơn thức nào sau đây?',o:['2x²','x+2','x²-1','2/x'],a:0},
{t:'algebra',q:'Nếu P(x)=x-3 thì nghiệm của P là?',o:['-3','0','1','3'],a:3},
{t:'stats',q:'Trung bình cộng của 4, 6, 8 là?',o:['5','6','7','8'],a:1},
{t:'stats',q:'Số lớn nhất trong 3, 9, 5, 7 là?',o:['3','5','7','9'],a:3},
{t:'stats',q:'Dãy 2, 4, 6, 8 có bao nhiêu giá trị?',o:['2','3','4','5'],a:2}
];

let current=[],submitted=false;

function startQuiz(type){
  current=type==='all'?[...Q]:Q.filter(x=>x.t===type);
  submitted=false;
  document.getElementById('quizArea').classList.add('show');
  document.getElementById('scoreBox').classList.remove('show');
  document.getElementById('quizTitle').textContent=type==='all'?'🌟 Đề tổng hợp Toán Đại Số 7':'📝 Bài tập: '+({fraction:'Số hữu tỉ',power:'Lũy thừa',ratio:'Tỉ lệ thức',algebra:'Đại số',stats:'Thống kê'}[type]);
  document.getElementById('count').textContent=current.length+' câu hỏi';
  document.getElementById('liveScore').textContent='0';
  let f=document.getElementById('quizForm');f.innerHTML='';
  current.forEach((x,i)=>{
    let d=document.createElement('div');
    d.className='question';
    d.id=`qbox_${i}`;
    d.innerHTML=`<h3>Câu ${i+1}: ${x.q}</h3><div class="options">${x.o.map((o,j)=>`<label><input type="radio" name="q${i}" value="${j}"> ${String.fromCharCode(65+j)}. ${o}</label>`).join('')}</div>`;
    f.appendChild(d);
  });
  document.getElementById('bar').style.width='0%';
  window.scrollTo({top:document.getElementById('quizArea').offsetTop-80,behavior:'smooth'});
}

function submitQuiz(){
  if(submitted)return;
  let score=0,answered=0;
  current.forEach((x,i)=>{
    let qBox=document.getElementById(`qbox_${i}`);
    let el=document.querySelector(`input[name="q${i}"]:checked`);
    if(el){
      answered++;
      if(Number(el.value)===x.a){
        score++;
        qBox.classList.add('correct');
      } else {
        qBox.classList.add('incorrect');
      }
    } else {
      qBox.classList.add('incorrect');
    }
  });
  let point=(score/current.length*10);
  let box=document.getElementById('scoreBox');
  box.classList.add('show');
  box.innerHTML=`<div class="big">${point.toFixed(1)}/10</div><h2>🎉 Hoàn thành bài!</h2><p><b>${score}/${current.length}</b> câu đúng • Đã trả lời ${answered}/${current.length} câu</p><p>${point>=8?'🌟 Rất tốt!':point>=5?'👍 Cố gắng thêm nhé!':'💪 Hãy xem lại lý thuyết và làm lại!'}</p>`;
  document.getElementById('liveScore').textContent=score;
  document.getElementById('bar').style.width=(score/current.length*100)+'%';
  submitted=true;
}
</script>
</body>
</html>
* hiện đáp án đúng sai khi làm xong câu hỏi , hiện nền xanh ở câu hỏi nếu làm đúng và nền đỏ ở câu làm sai , hiện đáp án đúng sau khi hoàn thành bài tập 

" kí hiệu phân số và các dấu dược thể hiện như sách giáo khoa , 

" các câu không lặp lại nhau mà soạn ngẫu nhiên từng đợt

" phần biểu thức trong phần tính toán tự nhập biểu thức chứ không cố định một biểu thức

" thêm mục hướng dẫn ở các phép tính toán 

" tối ưu hóa cho cả điện thoại lẫn máy tính vẫn sử dụng được 

" tạo hoạt họa và các hiệu ứng khi click vào 

" trong phần bài tập có giới hạn thời gian , thêm vào các câu đúng sai , toàn bộ câu hỏi được tính điểm như hình thức thi toán hiện nay 

" 

Đã cập nhật và hoàn thiện ứng dụng web học tập Toán Đại Số 7 theo toàn bộ các yêu cầu của bạn!

Biểu tượng HTML
index
 HTML 
Đang mở
Các tính năng và cải tiến đã tích hợp trong phiên bản này:
Hiển thị đáp án & Phản hồi trực quan:

Nền màu xanh lá (#f0fdf4) khi câu trả lời đúng.

Nền màu đỏ nhạt (#fef2f2) khi trả lời sai.

Hiển thị rõ ràng đáp án đúng chuẩn kèm lời giải thích chi tiết ngay bên dưới mỗi câu sau khi bấm Nộp bài.

Ký hiệu phân số và phép toán chuẩn SGK:

Tích hợp MathJax rendering các biểu thức phân số  
b
a
​
 , lũy thừa x 
n
 , tỉ lệ thức, căn thức... đẹp mắt, đúng chuẩn giao diện sách giáo khoa Toán 7 mới.

Ngẫu nhiên hóa câu hỏi (không lặp lại):

Thuật toán tráo đổi ngẫu nhiên Fisher-Yates Shuffle tự động chọn lọc câu hỏi khác nhau qua từng đợt luyện đề.

Tự nhập biểu thức đại số linh hoạt:

Cho phép người dùng tự nhập bất kỳ biểu thức đại số nào (Ví dụ: 2*x^2 + 3*x - 5 hoặc (x+1)/(x-2)) và tính giá trị tại x tùy chọn.

Mục Hướng dẫn chi tiết ở các công cụ tính toán:

Mỗi công cụ tính (Phân số, Lũy thừa, Tỉ lệ thức, Đại lượng tỉ lệ, Biểu thức, Thống kê...) đều bổ sung hộp hướng dẫn (Guide box) trực quan.

Tối ưu hóa đa nền tảng (Mobile & Desktop):

Thiết kế chuẩn Responsive bằng CSS Flexbox, Grid, và typography theo quy chuẩn viewport điện thoại lẫn máy tính.

Hoạt họa & Hiệu ứng tương tác:

Đổi màu nền Gradient chuyển động mềm mại, hiệu ứng hover/click nhẹ nhàng trên các nút bấm và thẻ chuyên đề.

Đồng hồ đếm ngược & Câu hỏi Đúng/Sai:

Đích thân trải nghiệm bài thi có đếm ngược thời gian (10 phút), tích hợp dạng câu hỏi Đúng/Sai cùng câu hỏi Trắc nghiệm 4 lựa chọn, tự động quy đổi ra thang điểm 10 chuẩn cấu trúc thi hiện nay.




Gemini là một AI và có thể mắc sai sót.

<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Toán Đại Số 7 - Học, Tính Toán & Luyện Tập Thông Minh</title>
<!-- MathJax for rendering textbook-style math formulas -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<style>
:root {
  --primary: #6c63ff;
  --primary-dark: #4b43c6;
  --secondary: #00c6ff;
  --accent: #7bed9f;
  --success: #2ed573;
  --danger: #ff4757;
  --warning: #ffa502;
  --bg-card: rgba(255, 255, 255, 0.95);
  --text: #1e293b;
  --text-muted: #64748b;
  --radius: 20px;
  --shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
  background: linear-gradient(-45deg, #6c63ff, #3a7bd5, #00d2ff, #2ed573);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
  color: var(--text);
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

header {
  padding: 30px 20px 15px;
  text-align: center;
  color: white;
  text-shadow: 0 4px 12px rgba(0,0,0,0.25);
}

header h1 {
  font-size: clamp(28px, 5vw, 46px);
  font-weight: 800;
  letter-spacing: -0.5px;
}

header p {
  font-size: clamp(14px, 2.5vw, 18px);
  opacity: 0.95;
  margin-top: 6px;
}

/* Responsive Sticky Nav */
nav {
  position: sticky;
  top: 10px;
  z-index: 100;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  max-width: 900px;
  margin: 10px auto;
  border-radius: 50px;
  padding: 8px 12px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  display: flex;
  justify-content: space-around;
  gap: 6px;
}

nav button {
  flex: 1;
  border: 0;
  border-radius: 30px;
  padding: 12px 16px;
  font-size: clamp(13px, 2vw, 15px);
  font-weight: 700;
  cursor: pointer;
  background: transparent;
  color: var(--text);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}

nav button.active, nav button:hover {
  background: var(--primary);
  color: white;
  box-shadow: 0 4px 15px rgba(108, 99, 255, 0.4);
  transform: translateY(-2px);
}

.container {
  max-width: 1100px;
  width: 95%;
  margin: 15px auto 40px;
  flex: 1;
}

.page { display: none; animation: fadeIn 0.4s ease-in-out; }
.page.active { display: block; }

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

.card {
  background: var(--bg-card);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  padding: 28px;
  margin-bottom: 25px;
  transition: transform 0.2s ease;
}

/* Home Grid */
.hero-title {
  text-align: center;
  font-size: 28px;
  color: var(--primary-dark);
  margin-bottom: 10px;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
  margin-top: 25px;
}

.topic-card {
  background: white;
  border-radius: 16px;
  padding: 25px;
  text-align: center;
  cursor: pointer;
  border: 2px solid #e2e8f0;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.topic-card:hover {
  transform: translateY(-6px) scale(1.02);
  border-color: var(--primary);
  box-shadow: 0 12px 25px rgba(108, 99, 255, 0.2);
}

.topic-card .icon { font-size: 48px; margin-bottom: 12px; }
.topic-card h3 { color: var(--primary-dark); margin-bottom: 8px; font-size: 20px; }
.topic-card p { color: var(--text-muted); font-size: 14px; line-height: 1.5; }

/* Subnav Buttons */
.subnav {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin: 18px 0;
}

.subnav button {
  background: #f1f5f9;
  border: 1.5px solid #cbd5e1;
  color: #334155;
  border-radius: 12px;
  padding: 8px 14px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s;
}

.subnav button.active, .subnav button:hover {
  background: var(--primary);
  color: white;
  border-color: var(--primary);
}

/* Lessons & Calculator Styles */
.lesson-content { display: none; }
.lesson-content.active { display: block; }
.lesson-content h3 { font-size: 22px; color: var(--primary-dark); margin-bottom: 12px; }

.formula-box {
  background: #eff6ff;
  border-left: 5px solid #3b82f6;
  padding: 16px;
  border-radius: 12px;
  margin: 14px 0;
  font-size: 18px;
  overflow-x: auto;
}

.guide-box {
  background: #fffbe6;
  border: 1.5px solid #ffe58f;
  border-radius: 12px;
  padding: 14px 18px;
  margin-bottom: 18px;
  font-size: 14px;
  color: #855800;
  line-height: 1.6;
}
.guide-box b { color: #d48800; }

.input-group {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 12px;
  margin-bottom: 15px;
}

.input-field {
  display: flex;
  flex-direction: column;
}

.input-field label {
  font-size: 13px;
  font-weight: 700;
  color: var(--text-muted);
  margin-bottom: 4px;
}

input, select {
  width: 100%;
  padding: 12px 14px;
  border: 2px solid #cbd5e1;
  border-radius: 12px;
  font-size: 15px;
  outline: none;
  transition: border 0.2s;
  background: white;
}

input:focus, select:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(108, 99, 255, 0.15);
}

.btn-action {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: white;
  border: none;
  padding: 14px 24px;
  border-radius: 14px;
  font-size: 16px;
  font-weight: 700;
  cursor: pointer;
  width: 100%;
  transition: all 0.2s ease;
  box-shadow: 0 4px 12px rgba(108, 99, 255, 0.3);
}

.btn-action:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 18px rgba(108, 99, 255, 0.4);
}

.btn-action:active {
  transform: translateY(0);
}

.result-card {
  margin-top: 20px;
  padding: 18px;
  border-radius: 14px;
  background: #f0fdf4;
  border-left: 5px solid var(--success);
  font-size: 16px;
  line-height: 1.8;
  display: none;
}

/* Practice Quiz Section */
.quiz-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
  background: white;
  padding: 18px;
  border-radius: 16px;
  margin-bottom: 20px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.05);
}

.timer-badge {
  background: #fff0f6;
  color: #c41d7f;
  border: 1.5px solid #ffadd2;
  padding: 8px 16px;
  border-radius: 30px;
  font-weight: 800;
  font-size: 16px;
  display: flex;
  align-items: center;
  gap: 6px;
}

.timer-badge.warning {
  background: #fff2e8;
  color: #d4380d;
  border-color: #ffbb96;
  animation: pulse 1s infinite;
}

@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.05); }
}

.question-card {
  background: white;
  border-radius: 16px;
  padding: 22px;
  margin-bottom: 20px;
  border-left: 6px solid var(--primary);
  box-shadow: 0 4px 12px rgba(0,0,0,0.04);
  transition: all 0.3s ease;
}

.question-card.correct-answer {
  border-left-color: var(--success) !important;
  background: #f0fdf4 !important;
}

.question-card.wrong-answer {
  border-left-color: var(--danger) !important;
  background: #fef2f2 !important;
}

.question-title {
  font-size: 17px;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 14px;
  display: flex;
  gap: 8px;
}

.type-tag {
  display: inline-block;
  font-size: 11px;
  font-weight: 800;
  padding: 3px 8px;
  border-radius: 6px;
  text-transform: uppercase;
}

.type-tag.mc { background: #e0f2fe; color: #0369a1; }
.type-tag.tf { background: #fef3c7; color: #b45309; }

.options-grid {
  display: grid;
  gap: 10px;
}

.option-item {
  display: flex;
  align-items: center;
  padding: 12px 16px;
  border: 2px solid #e2e8f0;
  border-radius: 12px;
  cursor: pointer;
  transition: all 0.2s;
  background: #f8fafc;
  font-size: 15px;
}

.option-item:hover {
  background: #f1f5f9;
  border-color: #cbd5e1;
}

.option-item input {
  width: auto;
  margin-right: 12px;
  cursor: pointer;
}

/* Correct / Wrong Badge Feedback */
.feedback-box {
  margin-top: 14px;
  padding: 12px 16px;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 600;
  display: none;
}

.feedback-box.correct {
  display: block;
  background: #dcfce7;
  color: #15803d;
  border: 1px solid #86efac;
}

.feedback-box.wrong {
  display: block;
  background: #fee2e2;
  color: #b91c1c;
  border: 1px solid #fca5a5;
}

/* Score Modal / Result */
.score-dashboard {
  text-align: center;
  padding: 30px;
  background: white;
  border-radius: 20px;
  box-shadow: var(--shadow);
  display: none;
}

.score-dashboard.show { display: block; animation: zoomIn 0.4s ease; }

@keyframes zoomIn {
  from { transform: scale(0.9); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

.big-score {
  font-size: 56px;
  font-weight: 900;
  color: var(--primary);
  margin: 10px 0;
}

footer {
  text-align: center;
  color: white;
  padding: 25px;
  font-size: 14px;
  margin-top: auto;
  text-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

@media (max-width: 640px) {
  nav { border-radius: 20px; padding: 6px; }
  nav button { padding: 8px 10px; font-size: 12px; }
  .card { padding: 18px; }
  .quiz-header { flex-direction: column; align-items: flex-start; }
}
</style>
</head>
<body>

<header>
  <h1>📚 TOÁN ĐẠI SỐ 7</h1>
  <p>Học Chuẩn SGK • Máy Tính Thông Minh • Luyện Đề Thi Tự Động Chấm</p>
</header>

<nav>
  <button id="nav-home" class="active" onclick="showPage('home')">🏠 Trang chủ</button>
  <button id="nav-theory" onclick="showPage('theory')">📖 Lý thuyết</button>
  <button id="nav-calc" onclick="showPage('calc')">🧮 Máy tính</button>
  <button id="nav-practice" onclick="showPage('practice')">📝 Luyện đề</button>
</nav>

<main class="container">

  <!-- HOME PAGE -->
  <section id="home" class="page active">
    <div class="card">
      <h2 class="hero-title">🌟 Bắt đầu hành trình chinh phục Toán 7</h2>
      <p style="text-align:center; color: var(--text-muted);">Hãy chọn một mục bên dưới để trải nghiệm học tập tương tác cao!</p>
      
      <div class="cards-grid">
        <div class="topic-card" onclick="showPage('theory')">
          <div class="icon">📖</div>
          <h3>Lý Thuyết SGK</h3>
          <p>Tóm tắt toàn bộ 10 chuyên đề Đại số 7 chuẩn chương trình mới với công thức trực quan.</p>
        </div>
        <div class="topic-card" onclick="showPage('calc')">
          <div class="icon">🧮</div>
          <h3>Công Cụ Tính Toán</h3>
          <p>Tự nhập biểu thức bất kỳ, tính phân số, tỉ lệ thức, thống kê có kèm hướng dẫn từng bước.</p>
        </div>
        <div class="topic-card" onclick="showPage('practice')">
          <div class="icon">📝</div>
          <h3>Luyện Đề Thi Trực Tuyến</h3>
          <p>Đề soạn ngẫu nhiên, có đồng hồ đếm ngược, câu hỏi Trắc nghiệm & Đúng/Sai chuẩn cấu trúc thi.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- THEORY PAGE -->
  <section id="theory" class="page">
    <div class="card">
      <h2>📖 Tổng Hợp Lý Thuyết Đại Số 7</h2>
      <div class="subnav" id="theory-nav">
        <button class="active" onclick="showLesson('lt1')">🔢 1. Số hữu tỉ</button>
        <button onclick="showLesson('lt2')">⚡ 2. Lũy thừa</button>
        <button onclick="showLesson('lt3')">📐 3. Tỉ lệ thức</button>
        <button onclick="showLesson('lt4')">📈 4. Tỉ lệ thuận</button>
        <button onclick="showLesson('lt5')">📉 5. Tỉ lệ nghịch</button>
        <button onclick="showLesson('lt6')">🧮 6. Biểu thức đại số</button>
        <button onclick="showLesson('lt7')">✏️ 7. Đơn thức</button>
        <button onclick="showLesson('lt8')">📊 8. Đa thức 1 biến</button>
        <button onclick="showLesson('lt9')">🎯 9. Nghiệm đa thức</button>
        <button onclick="showLesson('lt10')">📋 10. Thu thập & Thống kê</button>
      </div>

      <div id="lt1" class="lesson-content active">
        <h3>1. Tập hợp Số Hữu Tỉ (\(\mathbb{Q}\))</h3>
        <p>Số hữu tỉ là số viết được dưới dạng phân số \(\frac{a}{b}\) với \(a, b \in \mathbb{Z}, b \neq 0\).</p>
        <div class="formula-box">
          Phép cộng/trừ: \[ \frac{a}{m} + \frac{b}{m} = \frac{a+b}{m} \]<br>
          Phép nhân/chia: \[ \frac{a}{b} \cdot \frac{c}{d} = \frac{a \cdot c}{b \cdot d} \quad ; \quad \frac{a}{b} : \frac{c}{d} = \frac{a \cdot d}{b \cdot c} \]
        </div>
      </div>

      <div id="lt2" class="lesson-content">
        <h3>2. Lũy Thừa Với Số Mũ Tự Nhiên</h3>
        <p>Cho \(x \in \mathbb{Q}, n \in \mathbb{N}^*\): \(x^n = x \cdot x \cdots x\) (\(n\) thừa số \(x\)).</p>
        <div class="formula-box">
          Nhân hai lũy thừa cùng cơ số: \[ x^m \cdot x^n = x^{m+n} \]<br>
          Chia hai lũy thừa cùng cơ số: \[ x^m : x^n = x^{m-n} \quad (x \neq 0, m \ge n) \]<br>
          Lũy thừa của lũy thừa: \[ (x^m)^n = x^{m \cdot n} \]
        </div>
      </div>

      <div id="lt3" class="lesson-content">
        <h3>3. Tỉ Lệ Thức & Tính Chất Dãy Tỉ Số Bằng Nhau</h3>
        <p>Tỉ lệ thức là đẳng thức của hai tỉ số \(\frac{a}{b} = \frac{c}{d}\).</p>
        <div class="formula-box">
          Tính chất cơ bản: \[ \frac{a}{b} = \frac{c}{d} \implies a \cdot d = b \cdot c \]<br>
          Dãy tỉ số bằng nhau: \[ \frac{a}{b} = \frac{c}{d} = \frac{e}{f} = \frac{a+c+e}{b+d+f} = \frac{a-c+e}{b-d+f} \]
        </div>
      </div>

      <div id="lt4" class="lesson-content">
        <h3>4. Đại Lượng Tỉ Lệ Thuận</h3>
        <p>Nếu đại lượng \(y\) liên hệ với \(x\) theo công thức \(y = kx\) (với \(k\) là hằng số khác 0) thì \(y\) tỉ lệ thuận với \(x\) theo hệ số tỉ lệ \(k\).</p>
        <div class="formula-box">
          Tỉ số hai giá trị tương ứng luôn không đổi: \[ \frac{y_1}{x_1} = \frac{y_2}{x_2} = \dots = k \]
        </div>
      </div>

      <div id="lt5" class="lesson-content">
        <h3>5. Đại Lượng Tỉ Lệ Nghịch</h3>
        <p>Nếu \(y\) liên hệ với \(x\) theo công thức \(y = \frac{a}{x}\) hay \(x \cdot y = a\) (với \(a \neq 0\)) thì \(y\) tỉ lệ nghịch với \(x\).</p>
        <div class="formula-box">
          Tích hai giá trị tương ứng luôn không đổi: \[ x_1 \cdot y_1 = x_2 \cdot y_2 = \dots = a \]
        </div>
      </div>

      <div id="lt6" class="lesson-content">
        <h3>6. Biểu Thức Đại Số & Giá Trị Biểu Thức</h3>
        <p>Biểu thức đại số chứa chữ biểu thị các số. Thay chữ bằng giá trị số cụ thể để tính giá trị biểu thức.</p>
        <div class="formula-box">
          Ví dụ: Giá trị của \(A = 2x^2 - 3x + 1\) tại \(x = 2\) là: \[ A = 2(2)^2 - 3(2) + 1 = 8 - 6 + 1 = 3 \]
        </div>
      </div>

      <div id="lt7" class="lesson-content">
        <h3>7. Đơn Thức Một Biến</h3>
        <p>Đơn thức một biến là biểu thức đại số chỉ gồm một số hoặc tích của một số với lũy thừa biến đó.</p>
        <div class="formula-box">
          Đơn thức đồng dạng có cùng số mũ của biến.<br>
          Cộng/trừ đơn thức đồng dạng: \[ 3x^2 + 5x^2 = (3+5)x^2 = 8x^2 \]
        </div>
      </div>

      <div id="lt8" class="lesson-content">
        <h3>8. Đa Thức Một Biến</h3>
        <p>Đa thức một biến là tổng của những đơn thức của cùng một biến.</p>
        <div class="formula-box">
          Dạng thu gọn: \[ P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0 \]<br>
          Bậc của đa thức là số mũ lớn nhất của biến có hệ số khác 0.
        </div>
      </div>

      <div id="lt9" class="lesson-content">
        <h3>9. Nghiệm Của Đa Thức Một Biến</h3>
        <p>Nếu tại \(x = a\), đa thức \(P(x)\) có giá trị bằng 0 (tức \(P(a) = 0\)) thì \(a\) được gọi là một nghiệm của \(P(x)\).</p>
        <div class="formula-box">
          Ví dụ: \(x = 3\) là nghiệm của \(P(x) = 2x - 6\) vì \(2(3) - 6 = 0\).
        </div>
      </div>

      <div id="lt10" class="lesson-content">
        <h3>10. Thu Thập & Thống Kê Dữ Liệu</h3>
        <p>Các chỉ số cơ bản trong thống kê mô tả:</p>
        <div class="formula-box">
          Số trung bình cộng (\(\bar{X}\)): \[ \bar{X} = \frac{x_1 + x_2 + \dots + x_n}{n} \]<br>
          Mốt của dấu hiệu (\(M_0\)): Giá trị có tần suất xuất hiện nhiều nhất.
        </div>
      </div>
    </div>
  </section>

  <!-- CALCULATOR PAGE -->
  <section id="calc" class="page">
    <div class="card">
      <h2>🧮 Máy Tính Toán 7 & Hướng Dẫn Giải</h2>
      <div class="subnav" id="calc-nav">
        <button class="active" onclick="showCalc('c1')">➗ Tính Phân Số</button>
        <button onclick="showCalc('c2')">⚡ Lũy Thừa</button>
        <button onclick="showCalc('c3')">📐 Tỉ Lệ Thức</button>
        <button onclick="showCalc('c4')">📈 Tỉ Lệ Thuận/Nghịch</button>
        <button onclick="showCalc('c5')">🧮 Biểu Thức Tự Nhập</button>
        <button onclick="showCalc('c6')">🎯 Tìm Nghiệm ax + b = 0</button>
        <button onclick="showCalc('c7')">📋 Thống Kê Dữ Liệu</button>
      </div>

      <!-- Calc 1: Phân số -->
      <div id="c1" class="lesson-content active">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Nhập hai phân số \(\frac{a}{b}\) và \(\frac{c}{d}\). Máy tính sẽ tự động quy đồng mẫu số và thực hiện 4 phép tính (+, -, ×, :) chuẩn SGK.
        </div>
        <div class="input-group">
          <div class="input-field"><label>Tử số a</label><input type="number" id="fa" value="1"></div>
          <div class="input-field"><label>Mẫu số b (≠0)</label><input type="number" id="fb" value="2"></div>
          <div class="input-field"><label>Tử số c</label><input type="number" id="fc" value="1"></div>
          <div class="input-field"><label>Mẫu số d (≠0)</label><input type="number" id="fd" value="3"></div>
        </div>
        <button class="btn-action" onclick="calcFraction()">✨ Thực Hiện Phép Tính</button>
        <div id="res-c1" class="result-card"></div>
      </div>

      <!-- Calc 2: Lũy thừa -->
      <div id="c2" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Nhập cơ số \(a\) và số mũ \(n\) để tính \(a^n\), \(a^{-n}\).
        </div>
        <div class="input-group">
          <div class="input-field"><label>Cơ số a</label><input type="number" id="pow-a" value="2" step="any"></div>
          <div class="input-field"><label>Số mũ n</label><input type="number" id="pow-n" value="3"></div>
        </div>
        <button class="btn-action" onclick="calcPower()">✨ Tính Lũy Thừa</button>
        <div id="res-c2" class="result-card"></div>
      </div>

      <!-- Calc 3: Tỉ lệ thức -->
      <div id="c3" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Tìm \(x\) trong đẳng thức \(\frac{a}{b} = \frac{x}{d}\). Áp dụng tính chất tỉ lệ thức: \(x = \frac{a \cdot d}{b}\).
        </div>
        <div class="input-group">
          <div class="input-field"><label>Giá trị a</label><input type="number" id="rat-a" value="2"></div>
          <div class="input-field"><label>Giá trị b (≠0)</label><input type="number" id="rat-b" value="3"></div>
          <div class="input-field"><label>Giá trị d (≠0)</label><input type="number" id="rat-d" value="12"></div>
        </div>
        <button class="btn-action" onclick="calcRatio()">✨ Tìm x</button>
        <div id="res-c3" class="result-card"></div>
      </div>

      <!-- Calc 4: Tỉ lệ thuận/nghịch -->
      <div id="c4" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Nhập hai cặp giá trị tương ứng để tìm hệ số tỉ lệ \(k\) hoặc \(a\) và tìm \(y_2\).
        </div>
        <div class="input-group">
          <div class="input-field">
            <label>Loại đại lượng</label>
            <select id="prop-type">
              <option value="direct">Tỉ lệ thuận (y = kx)</option>
              <option value="inverse">Tỉ lệ nghịch (y = a/x)</option>
            </select>
          </div>
          <div class="input-field"><label>Giá trị x₁</label><input type="number" id="prop-x1" value="3"></div>
          <div class="input-field"><label>Giá trị y₁</label><input type="number" id="prop-y1" value="6"></div>
          <div class="input-field"><label>Giá trị x₂</label><input type="number" id="prop-x2" value="5"></div>
        </div>
        <button class="btn-action" onclick="calcProportion()">✨ Tính Hệ Số & y₂</button>
        <div id="res-c4" class="result-card"></div>
      </div>

      <!-- Calc 5: Biểu thức tự nhập -->
      <div id="c5" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Bạn có thể **TỰ NHẬP BẤT KỲ BIỂU THỨC NÀO** theo biến \(x\) (Ví dụ: <code>2*x^2 + 3*x - 5</code> hoặc <code>(x+1)/(x-2)</code>), sau đó nhập giá trị \(x\) để tính kết quả!
        </div>
        <div class="input-group">
          <div class="input-field" style="grid-column: span 2;">
            <label>Nhập biểu thức P(x)</label>
            <input type="text" id="custom-expr" value="2*x^2 + 3*x - 5" placeholder="Ví dụ: 3*x^3 - 2*x + 1">
          </div>
          <div class="input-field">
            <label>Giá trị của x</label>
            <input type="number" id="custom-x" value="2" step="any">
          </div>
        </div>
        <button class="btn-action" onclick="calcCustomExpr()">✨ Tính Giá Trị Biểu Thức</button>
        <div id="res-c5" class="result-card"></div>
      </div>

      <!-- Calc 6: Phương trình ax+b=0 -->
      <div id="c6" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Giải phương trình bậc nhất một biến \(ax + b = 0\).
        </div>
        <div class="input-group">
          <div class="input-field"><label>Hệ số a</label><input type="number" id="eq-a" value="2"></div>
          <div class="input-field"><label>Hệ số b</label><input type="number" id="eq-b" value="-6"></div>
        </div>
        <button class="btn-action" onclick="calcEquation()">✨ Tìm Nghiệm x</button>
        <div id="res-c6" class="result-card"></div>
      </div>

      <!-- Calc 7: Thống kê -->
      <div id="c7" class="lesson-content">
        <div class="guide-box">
          <b>📌 Hướng dẫn:</b> Nhập dãy số phân cách bởi dấu phẩy (dấu cách tự loại bỏ). Máy tính sẽ phân tích Trung bình cộng, Mốt, Max, Min.
        </div>
        <div class="input-field" style="margin-bottom:15px;">
          <label>Dãy số liệu</label>
          <input type="text" id="stat-input" value="7, 8, 9, 8, 10, 8, 6">
        </div>
        <button class="btn-action" onclick="calcStats()">✨ Phân Tích Thống Kê</button>
        <div id="res-c7" class="result-card"></div>
      </div>

    </div>
  </section>

  <!-- PRACTICE / QUIZ PAGE -->
  <section id="practice" class="page">
    <div class="card">
      <h2>📝 Luyện Đề Thi Trực Tuyến chuẩn SGK</h2>
      <p style="color:var(--text-muted); margin-bottom: 15px;">Đề ngẫu nhiên từng đợt • Có giới hạn thời gian • Gồm câu hỏi Trắc nghiệm 4 đáp án & Đúng/Sai chuẩn thi hiện nay.</p>
      
      <div class="subnav">
        <button class="active" onclick="startQuiz('mixed')">🎲 Đề Tổng Hợp Ngẫu Nhiên (10 phút)</button>
        <button onclick="startQuiz('rational')">🔢 Chuyên Đề Số Hữu Tỉ</button>
        <button onclick="startQuiz('algebra')">📊 Chuyên Đề Đa Thức & Biểu Thức</button>
      </div>

      <div id="quiz-container" style="display:none; margin-top: 20px;">
        <div class="quiz-header">
          <div>
            <h3 id="quiz-title" style="color:var(--primary-dark);">Đề Thi Trắc Nghiệm</h3>
            <span id="quiz-count" style="font-size: 14px; color: var(--text-muted);">Số câu: 0</span>
          </div>
          <div class="timer-badge" id="timer-box">
            ⏱️ Thời gian: <span id="time-display">10:00</span>
          </div>
        </div>

        <form id="quiz-form"></form>

        <button class="btn-action" style="margin-top: 20px; font-size: 18px;" onclick="submitQuiz(event)">🎯 NỘP BÀI THI & CHẤM ĐIỂM</button>
      </div>

      <!-- Score Dashboard -->
      <div id="score-dashboard" class="score-dashboard">
        <h2 style="color:var(--primary-dark);">🎉 TỔNG KẾT KẾT QUẢ BÀI THI</h2>
        <div class="big-score" id="final-score">0 / 10</div>
        <p id="final-details" style="font-size: 16px; color: #475569; margin-bottom: 15px;"></p>
        <p id="final-eval" style="font-size: 18px; font-weight: 700; color: var(--success); margin-bottom: 20px;"></p>
        <button class="btn-action" onclick="startQuiz('mixed')">🔄 Làm Đề Ngẫu Nhiên Mới</button>
      </div>

    </div>
  </section>

</main>

<footer>
  🎓 <b>Ứng Dụng Học & Luyện Thi Toán Đại Số 7</b> • Thiết Kế Trực Quan, Chuẩn SGK Mới
</footer>

<script>
// --- NAVIGATION SYSTEM ---
function showPage(pageId) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
  
  document.getElementById(pageId).classList.add('active');
  document.getElementById('nav-' + pageId).classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function showLesson(id) {
  document.querySelectorAll('#theory .lesson-content').forEach(l => l.classList.remove('active'));
  document.querySelectorAll('#theory-nav button').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  event.target.classList.add('active');
  if(window.MathJax) MathJax.typesetPromise();
}

function showCalc(id) {
  document.querySelectorAll('#calc .lesson-content').forEach(c => c.classList.remove('active'));
  document.querySelectorAll('#calc-nav button').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  event.target.classList.add('active');
  if(window.MathJax) MathJax.typesetPromise();
}

// --- MATH CALCULATOR FUNCTIONS ---
function gcd(a, b) {
  a = Math.abs(a); b = Math.abs(b);
  while (b) { let t = b; b = a % b; a = t; }
  return a;
}

function formatFrac(num, den) {
  if (den === 0) return 'Không xác định';
  if (num === 0) return '0';
  let g = gcd(num, den);
  num /= g; den /= g;
  if (den < 0) { num = -num; den = -den; }
  if (den === 1) return `\(${num}\)`;
  return `\(\frac{${num}}{${den}}\);
}

function calcFraction() {
  let a = parseInt(document.getElementById('fa').value) || 0;
  let b = parseInt(document.getElementById('fb').value) || 1;
  let c = parseInt(document.getElementById('fc').value) || 0;
  let d = parseInt(document.getElementById('fd').value) || 1;
  let res = document.getElementById('res-c1');

  if (b === 0 || d === 0) {
    res.style.display = 'block';
    res.innerHTML = '⚠️ <b>Lỗi:</b> Mẫu số phải khác 0!';
    return;
  }

  let sumN = a * d + b * c, sumD = b * d;
  let subN = a * d - b * c, subD = b * d;
  let mulN = a * c, mulD = b * d;
  let divN = a * d, divD = b * c;

  res.style.display = 'block';
  res.innerHTML = `
    <b>Kết quả chi tiết phép tính phân số:</b><br>
    ➕ <b>Tổng:</b> \(\frac{${a}}{${b}} + \frac{${c}}{${d}} = ${formatFrac(sumN, sumD)}\<br>
    ➖ <b>Hiệu:</b> \(\frac{${a}}{${b}} - \frac{${c}}{${d}} = ${formatFrac(subN, subD)}\<br>
    ✖️ <b>Tích:</b> \(\frac{${a}}{${b}} \cdot \frac{${c}}{${d}} = ${formatFrac(mulN, mulD)}\<br>
    ➗ <b>Thương:</b> \(\frac{${a}}{${b}} : \frac{${c}}{${d}} = ${formatFrac(divN, divD)}\
  `;
  if(window.MathJax) MathJax.typesetPromise();
}

function calcPower() {
  let a = parseFloat(document.getElementById('pow-a').value) || 0;
  let n = parseInt(document.getElementById('pow-n').value) || 0;
  let res = document.getElementById('res-c2');
  let ans = Math.pow(a, n);
  res.style.display = 'block';
  res.innerHTML = `🎯 <b>Giá trị lũy thừa:</b> \(${a}^{${n}} = ${ans}\)`;
  if(window.MathJax) MathJax.typesetPromise();
}

function calcRatio() {
  let a = parseFloat(document.getElementById('rat-a').value) || 0;
  let b = parseFloat(document.getElementById('rat-b').value) || 1;
  let d = parseFloat(document.getElementById('rat-d').value) || 1;
  let res = document.getElementById('res-c3');
  if (b === 0) { res.style.display = 'block'; res.innerHTML = '⚠️ b phải khác 0!'; return; }
  let x = (a * d) / b;
  res.style.display = 'block';
  res.innerHTML = `🎯 <b>Giá trị x tìm được:</b> \(x = \frac{${a} \cdot ${d}}{${b}} = ${x}\)`;
  if(window.MathJax) MathJax.typesetPromise();
}

function calcProportion() {
  let type = document.getElementById('prop-type').value;
  let x1 = parseFloat(document.getElementById('prop-x1').value) || 1;
  let y1 = parseFloat(document.getElementById('prop-y1').value) || 1;
  let x2 = parseFloat(document.getElementById('prop-x2').value) || 1;
  let res = document.getElementById('res-c4');

  res.style.display = 'block';
  if (type === 'direct') {
    let k = y1 / x1;
    let y2 = k * x2;
    res.innerHTML = `📈 <b>Hệ số tỉ lệ thuận:</b> \(k = \frac{y_1}{x_1} = ${k}\)<br>🎯 <b>Giá trị \(y_2\):</b> \(y_2 = k \cdot x_2 = ${y2}\)`;
  } else {
    let a = x1 * y1;
    let y2 = a / x2;
    res.innerHTML = `📉 <b>Hệ số tỉ lệ nghịch:</b> \(a = x_1 \cdot y_1 = ${a}\)<br>🎯 <b>Giá trị \(y_2\):</b> \(y_2 = \frac{a}{x_2} = ${y2}\)`;
  }
  if(window.MathJax) MathJax.typesetPromise();
}

function calcCustomExpr() {
  let exprStr = document.getElementById('custom-expr').value;
  let xVal = parseFloat(document.getElementById('custom-x').value) || 0;
  let res = document.getElementById('res-c5');
  res.style.display = 'block';

  try {
    // Safe evaluation of mathematical expression with x
    let cleanExpr = exprStr.replace(/\^/g, '**').replace(/x/g, `(${xVal})`);
    let val = Function(`'use strict'; return (${cleanExpr})`)();
    res.innerHTML = `🎯 <b>Thay \(x = ${xVal}\) vào biểu thức:</b><br>\(P(${xVal}) = ${val}\)`;
  } catch (e) {
    res.innerHTML = `⚠️ <b>Lỗi cú pháp biểu thức!</b> Hãy kiểm tra lại (VD dùng dấu * cho phép nhân: <code>2*x^2 + 3*x</code>).`;
  }
  if(window.MathJax) MathJax.typesetPromise();
}

function calcEquation() {
  let a = parseFloat(document.getElementById('eq-a').value) || 0;
  let b = parseFloat(document.getElementById('eq-b').value) || 0;
  let res = document.getElementById('res-c6');
  res.style.display = 'block';

  if (a === 0) {
    res.innerHTML = (b === 0) ? '♾️ <b>Phương trình có vô số nghiệm.</b>' : '❌ <b>Phương trình vô nghiệm.</b>';
  } else {
    let x = -b / a;
    res.innerHTML = `🎯 <b>Nghiệm của phương trình:</b> \(x = \frac{-(${b})}{${a}} = ${x}\)`;
  }
  if(window.MathJax) MathJax.typesetPromise();
}

function calcStats() {
  let raw = document.getElementById('stat-input').value;
  let arr = raw.split(',').map(s => parseFloat(s.trim())).filter(n => !isNaN(n));
  let res = document.getElementById('res-c7');
  res.style.display = 'block';

  if (arr.length === 0) {
    res.innerHTML = '⚠️ Vui lòng nhập dãy số hợp lệ!';
    return;
  }

  let sum = arr.reduce((a, b) => a + b, 0);
  let avg = (sum / arr.length).toFixed(2);
  let max = Math.max(...arr);
  let min = Math.min(...arr);

  // Mode calculation
  let freq = {};
  arr.forEach(n => freq[n] = (freq[n] || 0) + 1);
  let maxFreq = 0;
  for (let key in freq) { if (freq[key] > maxFreq) maxFreq = freq[key]; }
  let modes = [];
  for (let key in freq) { if (freq[key] === maxFreq) modes.push(key); }

  res.innerHTML = `
    📊 <b>Số lượng giá trị (N):</b> ${arr.length}<br>
    ➕ <b>Tổng các giá trị:</b> ${sum}<br>
    📈 <b>Trung bình cộng (\(\bar{X}\)):</b> ${avg}<br>
    ⭐ <b>Mốt của dấu hiệu (\(M_0\)):</b> ${modes.join(', ')} (xung quanh ${maxFreq} lần)<br>
    🔺 <b>Lớn nhất:</b> ${max} | 🔻 <b>Nhỏ nhất:</b> ${min}
  `;
  if(window.MathJax) MathJax.typesetPromise();
}

// --- DYNAMIC & RANDOMIZED QUIZ SYSTEM WITH TIMER ---
const QUESTION_BANK = [
  // Multi-choice (MC)
  { type: 'mc', topic: 'rational', q: 'Kết quả của phép tính \(\frac{1}{2} + \frac{1}{3}\) bằng bao nhiêu?', o: ['\(\frac{5}{6}\)', '\(\frac{2}{5}\)', '\(\frac{1}{6}\)', '\(\frac{3}{5}\)'], a: 0, exp: 'Quy đồng mẫu số 6: 3/6 + 2/6 = 5/6.' },
  { type: 'mc', topic: 'rational', q: 'Phân số nào sau đây biểu diễn số hữu tỉ âm?', o: ['\(\frac{-3}{-4}\)', '\(-\frac{2}{5}\)', '\(\frac{0}{7}\)', '\(\frac{4}{9}\)'], a: 1, exp: 'Phân số -2/5 có tử âm, mẫu dương nên là số hữu tỉ âm.' },
  { type: 'mc', topic: 'power', q: 'Giá trị của lũy thừa \(2^4\) là bao nhiêu?', o: ['8', '16', '12', '64'], a: 1, exp: '2^4 = 2 * 2 * 2 * 2 = 16.' },
  { type: 'mc', topic: 'power', q: 'Với \(a \neq 0\), kết quả của \(a^5 : a^2\) bằng:', o: ['\(a^3\)', '\(a^{10}\)', '\(a^7\)', '\(a^{2.5}\)'], a: 0, exp: 'Giữ nguyên cơ số, trừ số mũ: 5 - 2 = 3.' },
  { type: 'mc', topic: 'ratio', q: 'Từ tỉ lệ thức \(\frac{a}{b} = \frac{c}{d}\) (\(b,d \neq 0\)), ta suy ra đẳng thức nào?', o: ['\(a \cdot d = b \cdot c\)', '\(a \cdot b = c \cdot d\)', '\(a + c = b + d\)', '\(a \cdot c = b \cdot d\)'], a: 0, exp: 'Tích ngoại tỉ bằng tích trung tỉ: a * d = b * c.' },
  { type: 'mc', topic: 'algebra', q: 'Giá trị của biểu thức \(A = 2x^2 - 5\) tại \(x = 3\) là:', o: ['13', '7', '31', '1'], a: 0, exp: 'A = 2*(3)^2 - 5 = 2*9 - 5 = 13.' },
  { type: 'mc', topic: 'algebra', q: 'Bậc của đa thức \(P(x) = 4x^3 - 2x^5 + x - 7\) là:', o: ['5', '3', '4', '1'], a: 0, exp: 'Bậc của đa thức là số mũ lớn nhất của biến x (ở đây là 5).' },
  { type: 'mc', topic: 'algebra', q: 'Nghiệm của đa thức \(P(x) = 3x - 9\) là:', o: ['\(x = 3\)', '\(x = -3\)', '\(x = 0\)', '\(x = 9\)'], a: 0, exp: 'Cho 3x - 9 = 0 => 3x = 9 => x = 3.' },
  
  // True / False (TF)
  { type: 'tf', topic: 'rational', q: 'Khẳng định: "Số 0 không phải là số hữu tỉ dương cũng không phải là số hữu tỉ âm."', o: ['Đúng', 'Sai'], a: 0, exp: 'Theo định nghĩa SGK, số 0 thuộc tập Q nhưng không là số hữu tỉ âm hay dương.' },
  { type: 'tf', topic: 'power', q: 'Khẳng định: "Mọi số khác 0 khi nâng lên lũy thừa số mũ 0 đều bằng 1 (tức \(x^0 = 1\))."', o: ['Đúng', 'Sai'], a: 0, exp: 'Đúng theo quy ước lũy thừa số mũ 0.' },
  { type: 'tf', topic: 'ratio', q: 'Khẳng định: "Nếu đại lượng y tỉ lệ thuận với x thì x cũng tỉ lệ thuận với y."', o: ['Đúng', 'Sai'], a: 0, exp: 'Đúng! Vì y = kx => x = (1/k)y.' },
  { type: 'tf', topic: 'algebra', q: 'Khẳng định: "Biểu thức \(x + \frac{1}{x}\) là một đơn thức một biến."', o: ['Đúng', 'Sai'], a: 1, exp: 'Sai! Đơn thức không chứa phép cộng hoặc biến ở mẫu số.' }
];

let activeQuestions = [];
let quizTimer = null;
let secondsLeft = 600; // 10 minutes

function shuffleArray(array) {
  let arr = [...array];
  for (let i = arr.length - 1; i > 0; i--) {
    let j = Math.floor(Math.random() * (i + 1));
    [arr[i], arr[j]] = [arr[j], arr[i]];
  }
  return arr;
}

function startQuiz(type) {
  let pool = QUESTION_BANK;
  if (type === 'rational') pool = QUESTION_BANK.filter(q => q.topic === 'rational' || q.topic === 'power');
  if (type === 'algebra') pool = QUESTION_BANK.filter(q => q.topic === 'algebra' || q.topic === 'ratio');

  // Randomize questions each time!
  activeQuestions = shuffleArray(pool).slice(0, 8); // Select 8 random questions

  document.getElementById('quiz-container').style.display = 'block';
  document.getElementById('score-dashboard').classList.remove('show');
  document.getElementById('quiz-title').textContent = type === 'mixed' ? '🎲 Đề Thi Tổng Hợp (Ngẫu Nhiên)' : '📝 Đề Thi Theo Chuyên Đề';
  document.getElementById('quiz-count').textContent = `Tổng số: ${activeQuestions.length} câu hỏi`;

  // Render questions
  let form = document.getElementById('quiz-form');
  form.innerHTML = '';

  activeQuestions.forEach((q, i) => {
    let card = document.createElement('div');
    card.className = 'question-card';
    card.id = `qcard-${i}`;

    let tagText = q.type === 'mc' ? 'Trắc nghiệm 4 đáp án' : 'Đúng / Sai';
    let tagClass = q.type === 'mc' ? 'mc' : 'tf';

    let optionsHTML = q.o.map((opt, j) => `
      <label class="option-item">
        <input type="radio" name="q-${i}" value="${j}">
        <span>${opt}</span>
      </label>
    `).join('');

    card.innerHTML = `
      <div class="question-title">
        <span>Câu ${i+1}:</span>
        <span class="type-tag ${tagClass}">${tagText}</span>
        <div>${q.q}</div>
      </div>
      <div class="options-grid">${optionsHTML}</div>
      <div class="feedback-box" id="feedback-${i}"></div>
    `;

    form.appendChild(card);
  });

  if(window.MathJax) MathJax.typesetPromise();

  // Reset & start timer
  clearInterval(quizTimer);
  secondsLeft = 600;
  updateTimerDisplay();
  quizTimer = setInterval(() => {
    secondsLeft--;
    updateTimerDisplay();
    if (secondsLeft <= 0) {
      clearInterval(quizTimer);
      alert('⏰ Đã hết thời gian làm bài! Hệ thống tự động nộp bài.');
      autoSubmitQuiz();
    }
  }, 1000);

  window.scrollTo({ top: document.getElementById('quiz-container').offsetTop - 60, behavior: 'smooth' });
}

function updateTimerDisplay() {
  let m = Math.floor(secondsLeft / 60);
  let s = secondsLeft % 60;
  let disp = `${m.toString().padStart(2, '0')}:${s.toString().padStart(2, '0')}`;
  document.getElementById('time-display').textContent = disp;
  let timerBox = document.getElementById('timer-box');
  if (secondsLeft < 120) timerBox.classList.add('warning');
  else timerBox.classList.remove('warning');
}

function submitQuiz(e) {
  if (e) e.preventDefault();
  clearInterval(quizTimer);

  let correctCount = 0;

  activeQuestions.forEach((q, i) => {
    let card = document.getElementById(`qcard-${i}`);
    let feedback = document.getElementById(`feedback-${i}`);
    let selected = document.querySelector(`input[name="q-${i}"]:checked`);

    if (selected && parseInt(selected.value) === q.a) {
      correctCount++;
      card.className = 'question-card correct-answer';
      feedback.className = 'feedback-box correct';
      feedback.innerHTML = `✅ <b>Chính xác!</b> ${q.exp}`;
    } else {
      card.className = 'question-card wrong-answer';
      feedback.className = 'feedback-box wrong';
      let correctOptText = q.o[q.a];
      feedback.innerHTML = `❌ <b>Sai rồi!</b> Đáp án đúng là: <b>${correctOptText}</b>.<br>💡 <i>Giải thích:</i> ${q.exp}`;
    }
  });

  let point = ((correctCount / activeQuestions.length) * 10).toFixed(1);

  let dashboard = document.getElementById('score-dashboard');
  dashboard.classList.add('show');
  document.getElementById('final-score').textContent = `${point} / 10`;
  document.getElementById('final-details').textContent = `Bạn đã trả lời đúng ${correctCount} / ${activeQuestions.length} câu.`;
  
  let evalText = point >= 8.5 ? '🏆 Xuất sắc! Bạn nắm rất vững kiến thức Đại số 7!' : (point >= 6.5 ? '👍 Tốt! Hãy ôn lại các câu sai để đạt điểm tối đa.' : '💪 Cần cố gắng hơn! Xem kỹ lại phần lý thuyết nhé.');
  document.getElementById('final-eval').textContent = evalText;

  if(window.MathJax) MathJax.typesetPromise();
  window.scrollTo({ top: dashboard.offsetTop - 50, behavior: 'smooth' });
}

function autoSubmitQuiz() {
  submitQuiz(null);
}

// Initialize default MathJax view on load
window.onload = function() {
  if(window.MathJax) MathJax.typesetPromise();
};
</script>
</body>
</html>


1
