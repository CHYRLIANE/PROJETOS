# PROJETOS
Resumo do Projeto
Este script automatiza o seguinte processo: Gerar o boleto de parcelamento via ecac

Abre o menu Iniciar do Windows.
Digita e abre o navegador Chrome.
Navega até um URL específico (https://cav.receita.fazenda.gov.br/autenticacao/login), que é a página de login do portal da Receita Federal do Brasil.
Insere um CPF e uma senha.
Realiza o login e navega por diferentes páginas ou seções do portal, realizando várias ações de clique e digitação.
Ajustes Necessários
Ajuste dos tempos de espera: Dependendo da velocidade do seu computador e da conexão à internet, você pode precisar ajustar os tempos de espera (time.sleep) para garantir que as páginas carreguem completamente antes de prosseguir.
Verificação de erros: Considerar adicionar verificações para garantir que cada etapa foi concluída com sucesso antes de prosseguir para a próxima ação.
Segurança: Certifique-se de não armazenar senhas ou informações sensíveis em código aberto ou sem criptografia.
Após o boleto salvo o mesmo é enviado via whatzaap para o cliente.
Melhoria sempre serão bem vindas.

Código:
t pyautogui
import time

pyautogui.PAUSE = 1
# apertar o windows do teclado
pyautogui.press('win')
# digitar chrome
pyautogui.write("chrome")
# apertar enter
pyautogui.press('enter')
pyautogui.write('https://cav.receita.fazenda.gov.br/autenticacao/login')
pyautogui.press('enter')
#time.sleep(5)
#pyautogui.position()150181Mae
#Point(x=1214, y=649)
pyautogui.click(x=1223, y=661)
pyautogui.click()
time.sleep(5)   
pyautogui.write('cpf')
pyautogui.click(x=1596, y=742)
time.sleep(5)
pyautogui.write('senha')
pyautogui.press('enter')
time.sleep(3)
pyautogui.click(x=1544, y=345)
time.sleep(3)
pyautogui.click(x=928, y=575)
time.sleep(3)
pyautogui.write('cnpj')
time.sleep(3)
pyautogui.click(x=1057, y=568)
time.sleep(3)
pyautogui.click(x=343, y=455)
time.sleep(3)
pyautogui.click(x=378, y=927)
time.sleep(3)
pyautogui.click(x=104, y=536)
time.sleep(3)
pyautogui.click(x=812, y=674)
time.sleep(3)
pyautogui.click(x=1070, y=762)
# Caminho de origem para o arquivo que será enviado via WhatsApp
# Configurar a pausa padrão
pyautogui.PAUSE = 2
# Abrir o navegador Chrome
pyautogui.press('win')
pyautogui.write("chrome")
pyautogui.press('enter')

# Esperar até que o navegador seja aberto
time.sleep(5)

# Abrir o WhatsApp Web
pyautogui.write("web.whatsapp.com")
pyautogui.press('enter')

# Esperar até que o WhatsApp Web seja carregado
time.sleep(10)  # Ajuste conforme necessário

# Localizar o contato para enviar o arquivo,
pyautogui.click(x=192, y=315)
time.sleep(3)
pyautogui.write("nome do cliente do whats") 
time.sleep(3)
pyautogui.press('enter')

# Abrir o menu de anexo no WhatsApp Web
pyautogui.click(x=882, y=951)
time.sleep(3)
pyautogui.click(x=928, y=575)
time.sleep(3)
pyautogui.click(x=113, y=476)
time.sleep(3)
pyautogui.click
pyautogui.click(x=107, y=489)
time.sleep(3)
pyautogui.doubleClick(x=357, y=239)
time.sleep(3)
pyautogui.hotkey('ctrl', 'a')
# Pressiona a tecla Enter para confirmar a seleção
pyautogui.press('enter')
time.sleep(3)
pyautogui.press('enter')
pyautogui.hotkey('ctrl', 'w')

#Estou reconstruindo para retirar todas as coordenas e reconhecer pela imagem ,o site do ecac passará por atualizações ,já salvei algumas imagens para teste e vai dar certo
