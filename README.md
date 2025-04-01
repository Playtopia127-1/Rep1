<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
        }
        section {
            margin: 2em;
        }
        .container {
            background-color: white;
            padding: 1em;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .projects img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        .contact-form input, .contact-form textarea, .resume-upload input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .contact-form button, .resume-upload button {
            background-color: #333;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .contact-form button:hover, .resume-upload button:hover {
            background-color: #555;
        }
        .upload-box {
            border: 2px dashed #333;
            padding: 30px;
            border-radius: 8px;
            text-align: center;
            background-color: #fafafa;
            cursor: pointer;
        }
        .upload-box:hover {
            background-color: #f0f0f0;
        }
        .upload-box p {
            margin: 10px 0;
        }
        .hidden-input {
            display: none;
        }
        .upload-box.active {
            border-color: #ff4444;
        }
        .upload-btn {
            background-color: #333;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
        }
        .upload-btn:hover {
            background-color: #555;
        }
        .social-links a {
            margin: 0 10px;
            text-decoration: none;
            color: #333;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Bem-vindo ao Meu Portfólio</h1>
    </header>

    <section class="bio container">
        <h2>Sobre Mim</h2>
        <p>Sou um programador amador ainda. Com o objetivo de ser um programador profissional.</p>
    </section>

    <section class="projects container">
        <h2>Meus Projetos</h2>
        <div class="project">
            <h3>Projeto 1 - Jogo da Cobrinha</h3>
            <p>Jogo da Cobrinha (Snake Game) em HTML, CSS e JavaScript.</p>
            <a href="https://linkdoproj1.com" target="_blank">Veja o projeto</a>
            <img src="imagem-projeto1.jpg" alt="Imagem do projeto 1">
     <h3>Projeto 2 - Calculadora</h3>
            <p>Calculadora em HTML, CSS e JavaScript.</p>
            <a href="https://linkdoproj1.com" target="_blank">Veja o projeto</a>
            <img src="imagem-projeto1.jpg" alt="Imagem do projeto 2">
      <h3>Projeto 3 - Pong </h3>
            <p>Pong em HTML, CSS e JavaScript.</p>
            <a href="https://linkdoproj1.com" target="_blank">Veja o projeto</a>
            <img src="imagem-projeto1.jpg" alt="Imagem do projeto 3">
        </div>
    </section>

    <section class="skills container">
        <h2>Linguagens Dominadas</h2>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
            <li>Java</li>
            <li>Python</li>
            <li>C++</li>
            <li>C#</li>
            <li>SQL</li>
            <li>PHP</li> 
	  <h2>Outras Habilidades </h2>
        <ul>
            <li>Trabalho Cooperativo</li>
            <li>Sociavel</li>
            <li>Resolução de problemas</li>
            <li>Calculos rapidos</li>
            <li>Logica de Programação</li>
            <li>Wordpress</li>
        </ul>
    </section>

    <section class="contact container">
        <h2>Contato</h2>
        <div class="contact-form">
            <form action="mailto:Matheus19993106131@gmail.com" method="POST">
                <label for="name">Nome:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Mensagem:</label>
                <textarea id="message" name="message" rows="5" required></textarea>

                <button type="submit">Enviar</button>
            </form>
        </div>



    <section class="social-links container">
        <h2>Redes Sociais</h2>
        <a href="https://www.linkedin.com/in/seu-linkedin" target="_blank">LinkedIn</a>
        <a href="https://github.com/Playtopia127-1/Rep1" target="_blank">GitHub</a>
        <a href="https://www.instagram.com/seu-instagram" target="_blank">Instagram</a>
    </section>

    <footer>
        <p>&copy; 2025 Matheus Henrique Rufino de Moura. Todos os direitos reservados.</p>
    </footer>

    <script>
        const uploadBox = document.getElementById("uploadBox");
        const fileInput = document.getElementById("fileInput");
        const fileName = document.getElementById("fileName");

      
        uploadBox.addEventListener("click", () => fileInput.click());

        fileInput.addEventListener("change", (event) => {
            if (event.target.files.length > 0) {
                fileName.textContent = event.target.files[0].name;
                uploadBox.classList.add("active");
            }
        });

     
        uploadBox.addEventListener("dragover", (event) => {
            event.preventDefault();
            uploadBox.classList.add("active");
        });

        uploadBox.addEventListener("dragleave", () => {
            uploadBox.classList.remove("active");
        });

        uploadBox.addEventListener("drop", (event) => {
            event.preventDefault();
            if (event.dataTransfer.files.length > 0) {
                fileInput.files = event.dataTransfer.files;
                fileName.textContent = event.dataTransfer.files[0].name;
                uploadBox.classList.add("active");
            }
        });
    </script>

</body>
</html>
