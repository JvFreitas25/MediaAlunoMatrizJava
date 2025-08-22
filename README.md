# MediaAlunoMatrizJava
Montei outro código, com a intenção de melhorar meu último repositório. Desta vez fiz o uso de matrizes em Java para poder percorrer cada nota de cada aluno.

```java
package Matriz;

import java.util.Scanner;

public class MediaNotas {
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		
		System.out.print("Quantos alunos a turma tem? ");
		int qtdAlunos = sc.nextInt();
		System.out.print("Quantas notas por aluno? ");
		int qtdNotas = sc.nextInt();
		
		double[][] notasTurma = new double[qtdAlunos][qtdNotas];
		
		double somaAluno = 0;
		double mediaAluno = 0;
		
		for(int i = 0; i < notasTurma.length; i++) {
			for(int j = 0; j < notasTurma[i].length; j++) {
				System.out.printf("Digite a %d° do aluno %d: ", (j + 1), (i + 1));
				notasTurma[i][j] = sc.nextDouble();
				somaAluno += notasTurma[i][j];
			}
			
			mediaAluno = somaAluno / qtdNotas;
			System.out.println("Média Aluno "+ (i + 1) +": "+ mediaAluno);
			somaAluno = 0;
		}
		
		sc.close();
	}
}
```
