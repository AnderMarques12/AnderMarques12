<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <style>

        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
        .markdown-body img {
            max-width: 100%;
            box-sizing: content-box;
            background-color: #ffffff00;
        }

        
        .loading-visible {
            display: block;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .spinner {
    border: 8px solid #222;
    border-radius: 50%;
    border-top: 8px solid #ff0000;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    box-shadow: 0 0 20px rgba(255, 0, 0, 0.7);
}

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }

            100% {
                transform: rotate(360deg);
            }
        }

        #image-container img {
            max-width: 100%;
            height: auto;
        }

        .feedback-hidden {
    display: none;
    color: #ffffff;
    font-family: 'M PLUS 1 Code', monospace;
    margin-top: 10px;
}

#hack-feedback {
    font-size: 14px;
    text-align: center;
    margin-top: 20px;
    color: #00ff3d;
    background-color: rgba(0, 0, 0, 0.8);
    padding: 10px;
    border-radius: 5px;
    width: 100%;
    display: none; 
}

.context-options {
    display: none;
    position: fixed;
    top: 80%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgb(0, 0, 0);
    padding: 20px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000;
}

        .context-options img {
            width: 100px;
            margin: 0 auto 20px;
            display: block;
        }

        .context-options .bot-title {
    font-size: 16px;
    text-align: center;
    margin-bottom: 20px;
    color: #ffffff;
}

.context-options .context-option {
    font-size: 14px;
    display: block;
    padding: 12px 20px;
    margin-bottom: 5px;
    background-color: rgb(25, 0, 255); 
    border-radius: 5px;
    color: #ffffff;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.3s, transform 0.1s;

}

.context-options .context-option:hover {
    background-color: rgb(27 0 255 / 56%);
    transform: scale(1.05);
}

.context-options .closeContextOptions:hover {
    background-color: rgb(255 0 0 / 80%);

}
        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            margin-top: 20px;
        }

        html, body {
        margin: 0;
        padding: 0;
        overflow-x: hidden; 
        overflow-y: auto; 
        height: 100%; 
    }

    .login-wrapper {
        display: flex;
        align-items: center;
        justify-content: center;
        height: auto; 
        padding: 20px; 
        
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
        background-color: rgba(0, 0, 0, 0); 
    }

    .custom-container {
    text-align: center;
    max-width: 388px;
    width: 100%;
    padding: 0px;
    background-color: rgba(0, 0, 0, 0);
    border-radius: 23px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0);
}

        .login-intro-img {
            max-width: 100%;
            height: auto;
            margin-bottom: 7px;
        }

        .register-form h6 {
            color: #ffffff;
        }

        .register-form p {
            color: rgb(255, 255, 255);
        }
        .form-group {
    position: relative;
    margin-bottom: 30px;
}

.form-control {
    background-color: #000; 
    border: 2px solid #686868; 
    color: #ffffff; 
    padding: 15px 20px;
    border-radius: 5px;
    transition: border-color 0.3s ease, box-shadow 0.3s ease;
    font-size: 16px;
    box-shadow: 0 0 10px rgba(0, 255, 68, 0); 
}

.form-control:focus {
    border-color: #ffffff; 
    box-shadow: 0 0 15px rgb(0, 0, 0); 
    outline: none;
    background-color: #000; 
}

.form-control::placeholder {
    color: rgb(247, 247, 247); 
}


.btn-primary2 {
    background-color: #000000;
    border: 2px solid #00ff37;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgba(0, 255, 13, 0.507), 0 0 20px rgba(0, 255, 34, 0.3);
    position: relative;
    overflow: hidden;
}

.btn-primary1 {
    background-color: #000000;
    border: 2px solid #ff0000;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgba(255, 0, 0, 0.5), 0 0 20px rgba(255, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
}


.btn-primary1::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgba(255, 0, 0, 0.5);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}
.btn-primary2::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgba(0, 255, 42, 0.541);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}

.btn-primary1:hover::before {
    top: 0;
}
.btn-primary2:hover::before {
    top: 0;
}

.btn-primary1:hover {
    background-color: #000000;
    color: #000;
    box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
    transform: scale(1.05);
}
.btn-primary2:hover {
    background-color: #000000;
    color: #000;
    box-shadow: 0 0 30px rgb(44 255 0 / 80%);
    transform: scale(1.05);
}
.social-icons a.instagram {
    color: #C13584; 

}

.social-icons a.instagram:hover {
    color: #e1306c; 
    text-shadow: 0 0 15px rgba(225, 48, 108, 0.8);
}

.social-icons a.telegram {
    color: #0088cc; 

}

.social-icons a.telegram:hover {
    color: #00acee; 
    text-shadow: 0 0 15px rgba(0, 172, 238, 0.8);
}

.social-icons a.whatsapp {
    color: #25D366; 

}

.social-icons a.whatsapp:hover {
    color: #128C7E; 
    text-shadow: 0 0 15px rgba(18, 140, 126, 0.8);
}


.social-icons {
    margin-top: 20px;
    text-align: center;
}

.social-icons a {
    color: #ffffff;
    font-size: 2.5rem;
    margin: 0 15px;
    position: relative;
    transition: color 0.3s ease, transform 0.3s ease;

}
.social-icons a:hover {
    color: #ff0000; 
    transform: scale(1.2); 
    text-shadow: 0 0 15px rgba(255, 0, 0, 0.8), 0 0 30px rgba(255, 0, 51, 0.5); 
}


.social-icons a::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    background-color: #ffffff; 
    bottom: -5px;
    left: 0;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.4s ease, background-color 0.4s ease;
}

.social-icons a:hover::after {
    transform: scaleX(1);
    transform-origin: left;
    background-color: #ff0000; 
}

.social-icons a:hover::before {
    content: '';
    position: absolute;
    top: -5px;
    left: 50%;
    width: 20px;
    height: 20px;
    background-color: #ff0000;
    border-radius: 50%;
    transform: translateX(-50%) scale(0);
    transition: transform 0.4s ease;
}

.social-icons a:hover::before {
    transform: translateX(-50%) scale(1);
}

#iframe-container {
    display: none;
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: -12px;
    z-index: 9999;
}

    iframe {
        width: 100vw; 
        height: 150vh;
        border: none; 
    }
        .grid-container {
            display: grid;
            grid-template-columns: repeat(5, 50px);
            grid-template-rows: repeat(5, 50px);
            gap: 23px;
            height: 100%;
            width: 100%;
        }

        .grid-item {
            background-color: #00000000;
            border: 6px solid #00000000;
        }

        #draggable-image {
    position: absolute;
    top: 50px;
    left: 33px;
    z-index: 10002;
    cursor: move;
}

        #draggable-image img {
            width: 100px;
            height: auto;
        }

        .black-background {
            display: none;
        }
        
        .white-square {
    width: 593px;
    height: 646px;
    background-color: #ffffff00;
    border: 2px solid #00000000;
    position: absolute;
    top: -570px;
    left: -169px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 95px);
    grid-template-rows: repeat(5, 101px);
    gap: 21px;
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00;
    border: 11px solid #00000000;
}
.loading-hidden {
    display: none; 
}

.loading-visible {
    display: flex; 
    align-items: center;
    justify-content: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5); 
}
.large-icon {
    width: 111px;
    height: 53px;
}
.video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
        }

        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .controls {
            position: absolute;
            top: 20px;
            left: 20px;
            z-index: 1;
        }
        .student-count {
    display: block; 
}
.promo-banner {
    background-color: rgba(0, 0, 0, 0.85); /* Fundo escuro semi-transparente */
    border: 2px solid rgba(255, 0, 0, 0.3); /* Borda em vermelho */
    padding: 30px;
    text-align: center;
    margin: 20px 0;
    border-radius: 10px;
    box-shadow: 0px 0px 15px rgba(255, 0, 0, 0.4); /* Sombra vermelha suave */
    color: #fff;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.promo-banner:hover {
    transform: translateY(-5px); /* Efeito de elevação */
    box-shadow: 0px 0px 30px rgba(255, 0, 0, 0.7); /* Sombra vermelha mais forte no hover */
}

.promo-banner img {
    width: 130px;
    border-radius: 50%; /* Forma circular para a imagem */
    margin-bottom: 20px;
    box-shadow: 0px 0px 10px rgba(255, 0, 0, 0.5); /* Sombra vermelha na imagem */
}

.promo-banner h2 {
    font-size: 28px;
    margin-bottom: 15px;
    color: #ff3333; /* Vermelho claro */
}

.promo-banner p {
    font-size: 18px;
    color: #e0e0e0; /* Texto cinza claro */
    margin-bottom: 25px;
}

.preco-antigo {
    text-decoration: line-through;
    color: #ff4d4d; /* Vermelho para o preço antigo */
}

.preco-novo {
    color: #ff0000; /* Vermelho vibrante para o novo preço */
    font-size: 24px;
    font-weight: bold;
}

.promo-btn {
    background-color: #ff0000; /* Vermelho vibrante */
    color: #fff;
    padding: 12px 30px;
    text-decoration: none;
    font-size: 16px;
    font-weight: bold;
    border-radius: 5px;
    box-shadow: 0px 0px 20px rgba(255, 0, 0, 0.7); /* Sombra vermelha */
    transition: 0.3s ease;
}

.promo-btn:hover {
    background-color: #cc0000; /* Escurece o vermelho no hover */
    box-shadow: 0px 0px 40px rgba(255, 0, 0, 1); /* Efeito de sombra mais intenso */
    transform: scale(1.05); /* Aumenta levemente no hover */
}


.video-container {
    position: relative;
    padding-bottom: 56.25%; /* Proporção 16:9 */
    height: 0;
    overflow: hidden;
    max-width: 100%;
    background: #000; /* Cor de fundo opcional */
}

.video-container video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
h2.mt-3 {
    color: white; /* Define a cor branca */
    font-family: 'Roboto', sans-serif; /* Escolha uma fonte moderna e estilizada */
    font-size: 2.5rem; /* Ajuste o tamanho da fonte para um visual impactante */
    font-weight: bold; /* Torne o texto mais proeminente */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* Adicione uma leve sombra para dar profundidade */
    letter-spacing: 1px; /* Aumente o espaçamento entre as letras para um visual mais sofisticado */
}

    </style>
</head>

<body>
    <div class="video-background">
        <video autoplay="" loop="" muted="">
          <source src="https://doublejonwhite.com/Video2.mp4" type="video/mp4">
          
        </video>
      </div>
      

    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <p id="studentCount" class="mb-0" style="font-size: 39px; color: #00ff40; text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);">
                    <i class="fas fa-user-graduate" style="margin-right: 5px;"></i>
                    <span style="font-weight: bold;">1000 ALUNOS</span> / 
                    <span style="color: #ff0000; font-weight: bold;">LIMITE: 1000</span>
                </p>
                
                <img class="login-intro-img" src="https://i.ibb.co/8xfpYGj/fotor-20241011144526.png" alt="Perfil">
            </div>
            
            <div class="register-form mt-4">
                <p class="text-center mb-4">Digite sua senha e clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group mb-4">
                        <input type="password" id="password" placeholder="Digite sua senha" class="form-control" required>
                    </div>
                    <div class="row">
                        <div class="col">
                            <button class="btn btn-primary1 w-100" type="button" onclick="login('https://blaze1.space/pt/games/mines')" style="height: 60px;">
                                <img src="https://blaze1.space/static/media/logo.cf45d2ad.svg" alt="Logo" class="icon-small">
                                
                            </button>
                        </div>
                <div class="col">
                 <button class="btn btn-primary2 w-100" type="button" onclick="login('https://jon.bet/pt/games/double')" style="height: 60px;">
                         <img src="https://jon.bet/static/media/logo.3af9f796.svg" alt="Logo" class="large-icon">
                          
                        </button>
                  </div>
                      
                    
                  <div class="social-icons mt-3">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank" class="instagram"><i class="bi bi-instagram"></i></a>
                    <a href="https://t.me/hackermarquesz" target="_blank" class="telegram"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank" class="whatsapp"><i class="bi bi-whatsapp"></i></a>
                </div>
                
               
                    
                    <h2 class="mt-3">COMPRE AQUI!</h2>
                    <div class="promo-banner mt-3">
                        <img src="https://i.ibb.co/8K8JzJb/fotor-20241015202813.png" alt="Promoção Especial">
                        <h2>Somente 300 Vagas!</h2>
                        <p>De <span class="preco-antigo">R$ 549,99</span> por <span class="preco-novo">R$ 279,99</span></p>
                        <p><strong>Garanta já a sua vaga com esse super desconto!</strong></p>
                        <p>Restam apenas 300 vagas disponíveis, não perca!</p>
                        <a href="https://pay.sumup.com/b2c/Q711USGD" class="promo-btn">Aproveitar Agora</a>
                    </div>
                    
<div id="iframe-container">
<iframe id="login-iframe" src=""></iframe>

<div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
<img src="https://i.ibb.co/fpv7pmf/anonymous-8291223-1280.png" alt="Hacker"></div>

<div class="context-options" id="contextOptions">
<img id="myImage" src="https://i.ibb.co/8xfpYGj/fotor-20241011144526.png" alt="Imagem Atual">
<span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz </span>
<div id="result"></div>
<span class="context-option" onclick="stopScroll();"><i class="fa fa-bomb" aria-hidden="true"></i> Hackear Mines</span>
<span class="context-option closeContextOptions" onclick="closeContextOptions();"><i class="fa fa-play" aria-hidden="true"></i> Hackear Double</span>
<div id="loading-animation" class="loading-hidden">
<div class="spinner"></div>

</div>
                              

                                    
<div class="white-square">
    <div class="grid-container">
      
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
        

</div>                         
<div id="image-container"></div>
<div id="assertividade" class="assertivity-hidden"></div>
                        
</div>

    <div class="black-background"></div>
    <script>



document.addEventListener('DOMContentLoaded', function () {
            var video = document.getElementById('background-video');

            // Tenta reproduzir o vídeo quando a página é carregada
            video.play().then(() => {
                // Sucesso, o vídeo está sendo reproduzido
            }).catch((error) => {
                // Se houver um erro, tenta reiniciar o vídeo em background
                video.muted = true;
                video.play();
            });
        });
        function login(url) {
    const password = document.getElementById('password').value;
    if (password === 'ALUNO1098') {
        document.getElementById('loading-message').style.display = 'block';
        setTimeout(() => {
            document.getElementById('login-iframe').src = url;
            document.getElementById('iframe-container').style.display = 'block';
            document.getElementById('loading-message').style.display = 'none';
        }, 1000);
    } else {
        alert('Senha incorreta. Tente novamente.');
    }
}






    </script>
