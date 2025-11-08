رائع! 🌟 إليك النسخة الكاملة الجاهزة للتشغيل من تطبيق الملاحظات اليومية مع:

خلفية داكنة بتدرج مائل.

نصوص صفراء كالكتب القديمة.

خانة كتابة كبيرة وحواف مستديرة.

زر حفظ الملاحظة.

قائمة الملاحظات السابقة مع إمكانية التعديل.

ملاحظات افتراضية عند الفتح.

أيقونة جاهزة للتطبيق عند إضافة الملف للشاشة الرئيسية.

العمل بدون إنترنت.


> ملاحظة: ضع أي صورة مربعة باسم icon.png في نفس المجلد لإظهار الأيقونة.




---

<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>مذكراتي اليومية - داكن</title>

<!-- أيقونة التطبيق -->
<link rel="icon" type="image/png" sizes="192x192" href="icon.png">
<link rel="apple-touch-icon" href="icon.png">
<meta name="theme-color" content="#121212">

<style>
    body {
        background: linear-gradient(135deg, #121212, #1a1a1a, #222200);
        color: #FFD700;
        font-family: 'Courier New', monospace;
        margin: 0;
        padding: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    h1 { margin-bottom: 20px; }
    textarea {
        width: 90%;
        max-width: 600px;
        height: 120px;
        background-color: rgba(30,30,30,0.9);
        color: #FFD700;
        border: none;
        border-radius: 12px;
        padding: 10px;
        font-size: 16px;
        resize: none;
    }
    button {
        margin-top: 10px;
        padding: 10px 20px;
        font-size: 16px;
        border-radius: 12px;
        border: none;
        cursor: pointer;
        background-color: #FFD700;
        color: #121212;
        font-weight: bold;
        transition: 0.3s;
    }
    button:hover { background-color: #FFC107; }
    #notesList {
        margin-top: 20px;
        width: 90%;
        max-width: 600px;
    }
    .noteItem {
        background-color: rgba(30,30,30,0.9);
        color: #FFD700;
        padding: 10px;
        margin-bottom: 10px;
        border-radius: 12px;
        cursor: pointer;
        word-break: break-word;
    }
</style>
</head>
<body>
<h1>مذكراتي اليومية</h1>
<textarea id="noteInput" placeholder="اكتب ملاحظتك هنا..."></textarea>
<button onclick="saveNote()">حفظ الملاحظة</button>
<div id="notesList"></div>

<script>
let notes = JSON.parse(localStorage.getItem('dailyNotes')) || [
    'مرحبًا! هذه أول ملاحظتك الافتراضية.',
    'يمكنك تعديل أي ملاحظة بالنقر عليها.',
    'اضغط على حفظ لتخزين الملاحظات الجديدة.'
];

function displayNotes() {
    const notesList = document.getElementById('notesList');
    notesList.innerHTML = '';
    notes.forEach((note, index) => {
        const noteDiv = document.createElement('div');
        noteDiv.className = 'noteItem';
        noteDiv.innerText = note;
        noteDiv.onclick = () => editNote(index);
        notesList.appendChild(noteDiv);
    });
}

function saveNote() {
    const input = document.getElementById('noteInput');
    if(input.value.trim() !== '') {
        notes.push(input.value);
        localStorage.setItem('dailyNotes', JSON.stringify(notes));
        input.value = '';
        displayNotes();
    }
}

function editNote(index) {
    const newText = prompt('عدل ملاحظتك:', notes[index]);
    if(newText !== null) {
        notes[index] = newText;
        localStorage.setItem('dailyNotes', JSON.stringify(notes));
        displayNotes();
    }
}

displayNotes();
</script>
</body>
</html>


---

طريقة الاستخدام:

1. انسخ النص أعلاه في محرر نصوص.


2. احفظ الملف باسم:



dailyNotesDark.html

3. ضع صورة مربعة باسم icon.png في نفس المجلد.


4. افتح الملف بأي متصفح على الكمبيوتر أو الهاتف.


5. على الهاتف: اختر إضافة إلى الشاشة الرئيسية ليظهر التطبيق مع الأيقونة ويعمل كتطبيق مستقل.




---

إذا أحببت، أستطيع أن أكتب لك طريقة سريعة لتحويل هذا الملف إلى ZIP جاهز للتحميل المباشر بحيث تضغط عليه ويفتح التطبيق فورًا على أي جهاز، بدون أي خطوات إضافية.

هل تريد أن أفعل ذلك الآن؟
