def calculadora():
    print("Bem-vindo á Calculajhonson!")
    print("Só fazer o seu calculo \n")

    while True:
        try:
            num1 = float(input("Digite o primeiro número: "))
            operacao = input("Digite a operação (+, -, *, /): ").strip()
            num2 = float(input("Digite o segundo número: "))

            if operacao not in ['+', '-', '*', '/']:
                print("Erro: Operação inválida. Use apenas +, -, *, /")
                continue

            if operacao == '+':
                resultado = num1 + num2
            elif operacao == '-':
                resultado = num1 - num2
            elif operacao == '*':
                resultado = num1 * num2
            elif operacao == '/':
                if num2 == 0:
                    print("Erro: Não é possível dividir por zero!")
                    continue
                resultado = num1 / num2

            print(F"\nResultado: {num1} {operacao} {num2} = {resultado:.2f}\n!")

        except ValueError:
            print("Erro: Insira apenas números válidos (ex: 5 ou 3.14).")
            continue
        except Exception as e:
            print(f"Erro inesperado: {e}")
            break

        repetir = input("Deseja fazer outra operaçaõ ? (s/n): ").strip().lower()

        if repetir != 's':
            print("\nCalculadora encerrada. até jhonson!")
            break

if __name__ == "__main__":
    calculadora()
