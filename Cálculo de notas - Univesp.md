# Calculadora de aprovação Univesp

Um dos principais desejos de um estudante universitário é conhecer o seu status de aprovação em uma disciplina. Com esse objetivo em mente, foi desenvolvida uma aplicação para os estudantes da Univesp. Essa ferramenta permite que os alunos calculem se foram aprovados ou não com base em suas notas atuais e se preparem adequadamente para futuras avaliações, tendo plena consciência do que é necessário para alcançar a aprovação.

## Requisitos de aprovação

Conforme as diretrizes acadêmicas da Univesp, a aprovação requer que o aluno alcance uma média final igual ou superior a 5,0 (cinco). Para alcançar esse objetivo, é obrigatório realizar a Prova Regular, que possui um peso de 60% na composição da média, além de cumprir as atividades, que têm peso de 40%.

Em casos em que a média na disciplina seja inferior a 5,0 (cinco), o aluno é obrigado a fazer um exame presencial. Esse exame tem uma pontuação que varia de 0 (zero) a 10 (dez). A nota obtida no exame é somada à média anteriormente alcançada, e o resultado é dividido por dois para determinar a média final do aluno na respectiva disciplina.

## Passos para o cálculo

### 1 . Calcular nota de avaliação necessária para ser aprovado

```
nota_atividades = float(input("Qual a sua nota nas atividades semanais? "))
nota_avaliacao = (5 - (0.4 * nota_atividades))/0.6
print()
print(f"A nota mínima que você precisa na avaliação é: {nota_avaliacao:.2f}")
```

### 2. Verificar se você foi aprovado e calcular a nota necessária para o exame (caso necessário) 

```
nota_atividades = float(input("Qual a sua nota nas atividades semanais? "))
nota_avaliacao = float(input("Qual a sua nota da avaliação bimestral? "))
nota_final = (nota_atividades *0.4) + (nota_avaliacao * 0.6)
nota_minima_exame = (5*2)-nota_final
if nota_final >= 5:
  print()
  print(f"Parabéns, você foi aprovado. Sua nota foi: {nota_final:.2f}")
else:
  print()
  print(f"Não foi dessa vez, você precisará realizar o exame. Sua nota foi: {nota_final:.2f}. E sua nota mínima no exame para alcançar a aprovação é: {nota_minima_exame:.2f}")
```

### 3. Verificar se você foi aprovado pós exame

```
nota_final = float(input("Qual foi a sua nota final? "))
nota_exame = float(input("Qual a sua nota do exame? "))
media_final = (nota_final + nota_exame) / 2
if media_final >=5:
  print()
  print(f"Ufa, você conseguiu! Foi aprovado com a nota: {media_final:.2f}.")
else:
  print()
  print(f"Infelizmente não foi dessa vez, sua nota foi: {media_final:.2f}, você foi reprovado e necessitará realizar a matéria novamente.")
```
