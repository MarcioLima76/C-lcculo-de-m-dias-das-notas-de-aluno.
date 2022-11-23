# Código escrito em Python  para criar um programa de cáculo da média das notas dos alunos. 
print('Calculo da media dos alunos')

alunos = {}

while True:
    notas = []
    nome = input('Digite o nome do aluno: ')
    if nome =='':
        break

    for i in range(1, 5):
        nota = float(input('Digite a nota{}: '.format(i)))
        notas.append(nota)

    alunos[nome] = notas

for n in alunos.keys():
    media = (alunos[n][0] + alunos[n][1] + alunos[n][2] + alunos[n][3])  / 4
    a = alunos[n]
    print('Aluno: {} Nota1: {} Nota2: {} Nota3: {} Nota4 {} Media: {}'.format(n, a[0], a[1], a[2], a[3], media))

    if media >= 70:
        print('O aluno ', [n], 'obteve a media necessária e está aprovado!')

    elif 60 < media < 70:
        print('O aluno ', [n], ' NÃO obteve a media necessária e deverá fazer Recuperação!')

    else:
        print('O aluno ', [n], ' NÃO obteve a media mínima necessária e está Reprovado!')


