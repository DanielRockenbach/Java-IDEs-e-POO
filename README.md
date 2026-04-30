# Apresentação Java

<img width="306" height="164" alt="image" src="https://github.com/user-attachments/assets/0723f1c8-0722-4640-b8da-df2461023ae6" />


## Parte 1 - Histórico e Evolução do Java

### 1.1 Criação do Java e seus criadores
Java foi criado em 1995 por uma equipe da Sun Microsystems liderada por James Gosling, com colaboradores como Mike Sheridan e Patrick Naughton. O projeto começou em 1991 com o nome "Oak" e tinha o objetivo de criar uma linguagem portátil e segura para dispositivos eletrônicos.

### 1.2 Empresa responsável pelo Java antes e depois de 2010
- Antes de 2010: Sun Microsystems era a empresa responsável pelo desenvolvimento e manutenção do Java.
- Depois de 2010: Oracle Corporation adquiriu a Sun Microsystems em 2010 e passou a ser responsável pelo Java.

### 1.3 Objetivo principal do Java e impacto na programação moderna
O objetivo principal do Java era permitir que programas fossem escritos uma vez e executados em qualquer plataforma, seguindo o slogan "Write Once, Run Anywhere" (WORA). Isso foi possível graças à máquina virtual Java (JVM), que abstrai o hardware e o sistema operacional.

Impacto na programação moderna:
- Tornou o desenvolvimento multiplataforma mais acessível.
- Popularizou a programação orientada a objetos em aplicações corporativas.
- Estabeleceu padrões para desenvolvimento de sistemas distribuídos, aplicações web e backend.
- Influenciou outras linguagens e plataformas que também usam máquinas virtuais ou bytecode.

### 1.4 Principais versões do Java e mudanças significativas
- Java 1.0 (1996): primeira versão oficial, trouxe a API básica de coleções, threads, AWT e o compilador `javac`.
- Java 1.1 (1997): adicionou inner classes, JDBC, JavaBeans, RMI e suporte melhorado a internacionalização.
- Java 1.2 (1998): chamada de Java 2, marcou a introdução da plataforma J2SE, Swing e Collections Framework.
- Java 1.4 (2002): trouxe o pacote `java.nio`, assert, logging e melhorias de desempenho.
- Java 5 / 1.5 (2004): introduziu generics, annotations, enhanced for loop, autoboxing/unboxing, enum e concurrency utilities.
- Java 6 (2006): focou em melhorias de desempenho, scripting com `javax.script` e integração com web services.
- Java 7 (2011): adicionou try-with-resources, multi-catch, API de arquivos `java.nio.file` e o operador diamante `<>`.
- Java 8 (2014): uma das maiores mudanças, trouxe expressões lambda, streams, API de data/hora `java.time` e default methods em interfaces.
- Java 9 (2017): introduziu o sistema de módulos (Project Jigsaw), `jshell` e melhorias no GC.
- Java 11 (2018): primeira versão LTS após o novo ciclo de lançamentos, trouxe HTTP Client padrão, suporte a `var` em lambda parâmetros e ainda mais APIs de utilidade.
- Java 17 (2021): LTS com selamento de classes (`sealed`), padrões para `switch`, e melhorias no GC e performance.
- Java 21 (2023): LTS mais recente, trouxe record patterns, virtual threads (Project Loom) em preview e melhorias de performance e usabilidade.

> Nota: esta lista cobra as versões mais relevantes até os anos mais recentes. O Java continua evoluindo com lançamentos semestrais.

## Parte 2 - Ambientes de Desenvolvimento (IDEs)

### 2.1 IntelliJ IDEA
- Site: https://www.jetbrains.com/idea/
- Descrição: IDE comercial da JetBrains, reconhecida pela excelente inteligência de código, refatoração, suporte a frameworks e integrações.
- Vantagens:
  - Autocompletar e navegação de código muito avançados.
  - Suporte integrado a Spring, Maven, Gradle, Docker e testes.
  - Interface intuitiva e personalizável.
- Desvantagens:
  - Versão completa (Ultimate) é paga.
  - Pode consumir mais memória em máquinas mais antigas.
  <img width="2400" height="1478" alt="image" src="https://github.com/user-attachments/assets/bc780ba7-c1b9-462f-99ed-ddcd9fd36853" />


### 2.2 Eclipse
- Site: https://www.eclipse.org/
- Descrição: IDE open source muito utilizada para desenvolvimento Java, com grande ecossistema de plugins.
- Vantagens:
  - Gratuito e de código aberto.
  - Grande comunidade e muitos plugins disponíveis.
  - Bom suporte para projetos Java EE e OSGi.
- Desvantagens:
  - Interface menos moderna que outras IDEs.
  - Às vezes pode ser mais lento e complexo de configurar.
  <img width="797" height="497" alt="image" src="https://github.com/user-attachments/assets/a84be71e-3672-4bf6-bf1c-a63b6bfca4f6" />


### 2.3 NetBeans
- Site: https://netbeans.apache.org/
- Descrição: IDE open source mantida pela Apache Foundation, com suporte nativo a Java SE, Java EE e JavaFX.
- Vantagens:
  - Fácil de usar e boa integração com ferramentas Java padrão.
  - Ideal para iniciantes, com suporte rápido a projetos maven.
  - Gratuito e com bom suporte a visualização de GUI.
- Desvantagens:
  - Menos plugins e extensões comparado a Eclipse e IntelliJ.
  - Performance e usabilidade podem ser inferiores em projetos muito grandes.
  <img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/b84fb863-5a38-4383-aacd-e108df5fc260" />


### 2.4 Qual IDE escolheria para estudar?
Eu escolheria o IntelliJ IDEA (versão Community ou Ultimate, se disponível) porque oferece a melhor experiência de produtividade, revisão de código e suporte a frameworks modernos. Para estudo, sua capacidade de sugerir correções, navegação rápida e integração com ferramentas Java facilita o aprendizado e o desenvolvimento contínuo.

## Parte 3 - Paradigma de Programação Orientado a Objetos (POO)

### 3.1 Classe
Uma classe é um molde ou estrutura que define atributos e comportamentos comuns de um conjunto de objetos.

Exemplo:
```java
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    public String getNome() {
        return nome;
    }

    public int getIdade() {
        return idade;
    }
}
```

### 3.2 Objeto
Um objeto é uma instância de uma classe, contendo valores reais para os atributos definidos pela classe.

Exemplo:
```java
Pessoa p = new Pessoa("Ana", 25);
System.out.println(p.getNome() + " tem " + p.getIdade() + " anos.");
```

### 3.3 Encapsulamento
Encapsulamento é a técnica de esconder os detalhes internos de uma classe e expor apenas o que é necessário por meio de métodos públicos.

Exemplo:
```java
public class Conta {
    private double saldo;

    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
        }
    }

    public double getSaldo() {
        return saldo;
    }
}
```

### 3.4 Herança
Herança permite que uma classe (subclasse) herde atributos e métodos de outra classe (superclasse).

Exemplo:
```java
public class Animal {
    public void comer() {
        System.out.println("O animal está comendo.");
    }
}

public class Cachorro extends Animal {
    public void latir() {
        System.out.println("O cachorro está latindo.");
    }
}
```

### 3.5 Polimorfismo
Polimorfismo é a capacidade de um objeto ser tratado de diferentes formas, geralmente por meio de herança ou interfaces.

Exemplo:
```java
public class Animal {
    public void emitirSom() {
        System.out.println("Som genérico.");
    }
}

public class Gato extends Animal {
    @Override
    public void emitirSom() {
        System.out.println("Miau.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal meuAnimal = new Gato();
        meuAnimal.emitirSom(); // Imprime "Miau."
    }
}
```

## Parte 4 - Mercado de Trabalho para Desenvolvedores Java

### 4.1 Salário médio no Brasil
- Júnior: entre R$ 3.000 e R$ 5.000 por mês.
- Pleno: entre R$ 7.000 e R$ 12.000 por mês.
- Sênior: entre R$ 15.000 e R$ 25.000 por mês.

> Esses valores podem variar conforme localização, porte da empresa, benefícios e habilidades específicas.

### 4.2 Cinco áreas onde o Java é amplamente utilizado
1. Desenvolvimento web (backend com Spring Boot, Jakarta EE).
2. Desenvolvimento mobile (Android).
3. Sistemas corporativos e enterprise.
4. Aplicações de backend e microserviços.
5. Big data e processamento distribuído (Hadoop, Apache Flink).

### 4.3 Cinco tecnologias ou frameworks exigidos pelas empresas Java
1. Spring Boot / Spring Framework
2. Hibernate / JPA
3. Jakarta EE / Java EE
4. Maven ou Gradle
5. APIs REST e microserviços

---

### Observações finais
Este documento reúne um resumo completo sobre a história e evolução do Java, ambientes de desenvolvimento, conceitos de POO e o mercado de trabalho no Brasil. Para completar o trabalho, recomendo inserir capturas de tela reais das IDEs no espaço indicado em cada seção.
