# TRIANGULO

Quarto exercício sobre herança

## 🚀 Enunciado

Crie um projeto no com um pacote chamado utilidades e dentro uma classe chamada FuncoesUteis com os métodos:

Soma(int, int) que retorna a soma dos parâmetros;

Triangulo(int altura) que exibe um triângulo com a altura especificada. Exemplo:

x

xx

xxx

xxxx

Xxxxx

printArquivo(String arquivo) que lê um arquivo de texto e imprime seu conteúdo.

Crie a classe Main em outro pacote e teste as funções da classe FuncoesUteis.

### 📋 Pré-requisitos

package uteis;

import java.io.FileReader;
import java.io.BufferedReader;
import java.io.IOException;

public class FuncoesUteis {

    
    public int Soma(int a, int b) { //Aqui começo usando o método que retorna a soma de dois números     
        return a + b;
    }

    
    public void Triangulo(int altura) { // E aqui uso o método que imprime um triângulo com altura definida
        for (int i = 1; i <= altura; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("x");
            }
            System.out.println(); 
        }
    }

    
    public void printArquivo(String nomeArquivo) { //Aqui o método que lê o conteúdo de um arquivo e imprime na tela
        try {
            FileReader fr = new FileReader(nomeArquivo);
            BufferedReader br = new BufferedReader(fr);
            String linha;
            while ((linha = br.readLine()) != null) {
                System.out.println(linha);
            }
            br.close(); // Fechando o arquivo
        } catch (IOException e) {
            System.out.println("Erro ao abrir o arquivo: " + e.getMessage());
        }
    }
}
///////////////////////////////////////////////////////////////////////////////////////
package main;

import uteis.FuncoesUteis;

public class Main {
    public static void main(String[] args) {
        FuncoesUteis util = new FuncoesUteis();
        
      
        int resultado = util.Soma(3, 7);  //Aqui estou testando o método de soma
        System.out.println("Soma: " + resultado);
        
        
        System.out.println("Triângulo de altura 4:"); //Aqui o método do triângulo
        util.Triangulo(4);
        
        
        System.out.println("Conteúdo do arquivo 'teste.txt':"); // E por último testo o método de imprimir o arquivo (assumindo que existe um arquivo chamado "teste.txt")
        util.printArquivo("teste.txt");
    }

### 🔧 Instalação

* Explicação de como deve ser utilizado o projeto

## 🛠️ Construído com

Ferramentas utilizadas e bibliotecas

* IDE Eclipse

## 📌 Versão

* **Versão 1.0** caso seja atualizado manter a descrição inicial e inserir uma nova linha com descrição da atualização.
* **Versão 1.1** - *Refatoração* *data 09/09/24*

## ✒️ Autores

* João Carlos Ferreira de Araujo RA 248152 - AC2

