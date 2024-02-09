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
        <p>Като 1 умен и забавен човек, реших да ти задам няколко въпроса, въпроса е дали ще можеш да стигнеш до края на малкият тест?</p>
        <button onclick="question1()">Започни</button>
      `;
    }

    function question1() {
      document.body.innerHTML = `
        <h1>Въпрос 1</h1>
        <p>Какво харесвате повече? </p>
        <button onclick="question2('Разходка в парка')">Разходка в парка</button>
        <button onclick="question2('Разговор на пейка')">Разговор на пейка</button>
      `;
    }

    function question2(indentationStyle) {
      document.body.innerHTML = `
        <h1>Question 2</h1>
        <p>Знаеш ли, според подателя на този въпросник (Камен) кой има най-хубавата усмивка?👀 (Попълни с име)</p>
        <input type="text" id="programmingLanguage">
        <button onclick="question3('${indentationStyle}')">Продължи</button>
      `;
    }

    function question3(indentationStyle) {
      const programmingLanguage = document.getElementById('programmingLanguage').value;

      document.body.innerHTML = `
        <h1>Question 3</h1>
        <p>Готова ли сте, <strong>Нермин</strong> за  ${indentationStyle} (Моля направете снимка от тази страница)</p>
        <button onclick="showResult(true)">Продължи</button>
    
      `;
    }

    function showResult(isMatch) {  
      if (isMatch) {
        document.body.innerHTML = `
          <h1>Честито!</h1>
          <p>Ти си спечели среща с въпросният господин, сега трябва да му изпратите снимка на предната страница от този уебсайт, и също така дата удобна за вас.</p>
          
        `;
    } 
    
    
        }

  </script>
</body>
</html>
