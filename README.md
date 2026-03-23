# prompt_Engineering_Architecture-Aula04
# ================================
# SISTEMA SIMPLES DE CADASTRO E LOGIN
# ================================

# Dicionário para armazenar os usuários
# Estrutura: { "usuario": "senha" }
usuarios = {}


# --------------------------------
# FUNÇÃO PARA CADASTRAR USUÁRIO
# --------------------------------
def cadastrar():
    print("\n=== CADASTRO ===")
    
    # Solicita o nome de usuário
    username = input("Digite um nome de usuário: ")
    
    # Verifica se o usuário já existe
    if username in usuarios:
        print("Usuário já existe! Tente outro.")
        return  # Encerra a função
    
    # Solicita a senha
    senha = input("Digite uma senha: ")
    
    # Armazena no dicionário
    usuarios[username] = senha
    
    print("Cadastro realizado com sucesso!")


# --------------------------------
# FUNÇÃO PARA FAZER LOGIN
# --------------------------------
def login():
    print("\n=== LOGIN ===")
    
    # Solicita o usuário
    username = input("Digite seu usuário: ")
    
    # Verifica se o usuário existe
    if username not in usuarios:
        print("Usuário não encontrado!")
        return
    
    # Solicita a senha
    senha = input("Digite sua senha: ")
    
    # Verifica se a senha está correta
    if usuarios[username] == senha:
        print("Login realizado com sucesso!")
    else:
        print("Senha incorreta!")


# --------------------------------
# FUNÇÃO PRINCIPAL (MENU)
# --------------------------------
def menu():
    while True:
        print("\n=== MENU ===")
        print("1 - Cadastrar")
        print("2 - Login")
        print("3 - Sair")
        
        # Escolha do usuário
        opcao = input("Escolha uma opção: ")
        
        # Estrutura de decisão
        if opcao == "1":
            cadastrar()
        elif opcao == "2":
            login()
        elif opcao == "3":
            print("Encerrando o programa...")
            break  # Sai do loop
        else:
            print("Opção inválida! Tente novamente.")


# --------------------------------
# EXECUÇÃO DO PROGRAMA
# --------------------------------
menu()

<img width="1170" height="559" alt="image" src="https://github.com/user-attachments/assets/4e704f58-b83a-4c0a-b0d1-70fd7c5ed5d1" />
