<!DOCTYPE html>
<html>
<head>
  <title>Лексикон</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }

    h1 {
      color: #333;
    }

    button {
      padding: 10px 20px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Добър ден!</h1>

  <button onclick="startInvitation()">Започни</button>

  <script>
    function startInvitation() {
      document.body.innerHTML = `
        <h1>Здравей</h1>
        <p>Най-вероятно вече съм ти споменал, че това е нещо за работа/университет или нещо подобно, но пък е анкета за попълване специално правена за теб</p>
        <button onclick="question1()">Започни</button>
      `;
    }

    function question1() {
      document.body.innerHTML = `
        <h1>Въпрос 1</h1>
        <p>Какво харесваш повече? </p>
        <button onclick="question2('Разходка')">Разходка с Ками</button>
        <button onclick="question2('Разговор')">Разговор с Ками </button>
      `;
    }

    function question2(indentationStyle) {
      document.body.innerHTML = `
        <h1>Question 2</h1>
        <p>Коя е най-красивата принцеска според Камен 👀 (Попълни с име)</p>
        <input type="text" id="programmingLanguage">
        <button onclick="question3('${indentationStyle}')">Продължи</button>
      `;
    }

    function question3(indentationStyle) {
      const programmingLanguage = document.getElementById('programmingLanguage').value;

      document.body.innerHTML = `
        <h1>Question 3</h1>
        <p>Готова ли си, за последната част от анкетата? Моля информирай ме, след като попълниш на лексикона!
        <button onclick="showResult(true)">Продължи</button>
    
      `;
    }

    function showResult(isMatch) {  
      if (isMatch) {
        document.body.innerHTML = `
          <h1>Честито!</h1>
          <p>Ти си спечели среща с въпросният господин и той също печели, моля изпрати ми дата удобна за теб. Анкетата си е анкета все пак, трябва да се спази регламент!</p>
          
        `;
    } 
    
    
        }

  </script>
</body>
</html>
