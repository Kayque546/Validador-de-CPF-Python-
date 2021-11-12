# Validador-de-CPF-Python-
Algorítimo na linguagem Python que tem a função de validar os CPF's digitados.

print("Informe seu CPF:")
cpf = input()
n1 = int(cpf[0])
n2 = int(cpf[1])
n3 = int(cpf[2])
n4 = int(cpf[3])
n5 = int(cpf[4])
n6 = int(cpf[5])
n7 = int(cpf[6])
n8 = int(cpf[7])
n9 = int(cpf[8])
n10 = int(cpf[9])
n11 = int(cpf[10])

primeira_soma = (n1 * 10) + (n2 * 9) + (n3 * 8) + (n4 * 7) + (n5 * 6) + (n6 * 5) + (n7 * 4) + (n8 * 3) + (n9 * 2)
primeiro_digito = primeira_soma % 11
if primeiro_digito < 2:
    primeiro_digito = 0
else:
    primeiro_digito = 11 - primeiro_digito

segunda_soma = (n1 * 11) + (n2 * 10) + (n3 * 9) + (n4 * 8) + (n5 * 7) + (n6 * 6) + (n7 * 5) + (n8 * 4) + (n9 * 3) + (primeiro_digito * 2)
segundo_digito = segunda_soma % 11
if segundo_digito < 2:
    segundo_digito = 0
else:
    segundo_digito = 11 - segundo_digito

if primeiro_digito == n10 and segundo_digito == n11:
    print("Seu CPF é válido!")
else:
    print("Esse CPF é inválido!")
print("Verificação conclúida.")
