# PROJETO

Nesse projeto apresentaremos orientações formalizadas com a Linguagem de Modelagem Unificada para a construção de um sistema universitário. 
Aplicamos diagramas de casos de uso, diagramas de classes, e cenários de casos de usos, com objetivo de fornecer ferramentas de análise, design e implementação de sistemas baseados em software. 

# DIAGRAMA DE CASOS DE USO 
![image](https://github.com/RenanLeone/PTI/assets/145399765/51a1136c-a58f-4d0b-b871-a8a6e640fa88)

# DIAGRAMA DE CLASSES 
![image](https://github.com/RenanLeone/PTI/assets/145399765/fe9232a5-75c2-46e3-9c58-855c0130bbc2)
![image](https://github.com/RenanLeone/PTI/assets/145399765/39e97196-f9e7-462f-a1ca-9a92b674c402)

# TÉCNOLOGIA ULTILIZADA 
Java

# CODIGO PARA CADASTRO DE ALUNOS
```java
import java.util.Scanner;

public class CadastroAlunos {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Digite o nome do aluno: ");
        String nome = input.nextLine();

        System.out.print("Digite a data de nascimento do aluno (dd/mm/aaaa): ");
        String dataNascimento = input.nextLine();

        System.out.print("Digite o endereço do aluno: ");
        String endereco = input.nextLine();

        System.out.print("Digite o gênero do aluno: ");
        String genero = input.nextLine();

        System.out.println("\n--- Dados do Aluno ---");
        System.out.println("Nome: " + nome);
        System.out.println("Data de Nascimento: " + dataNascimento);
        System.out.println("Endereço: " + endereco);
        System.out.println("Gênero: " + genero);

        input.close();
    }
}
```
# CODIGO PARA CADASTRO DE PROFESSORES 
```java
import java.util.Scanner;

public class CadastroProfessores {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Digite o nome do professor: ");
        String nome = input.nextLine();

        System.out.print("Digite a data de nascimento do professor (dd/mm/aaaa): ");
        String dataNascimento = input.nextLine();

        System.out.print("Digite o endereço do professor: ");
        String endereco = input.nextLine();

        System.out.print("Digite o gênero do professor: ");
        String genero = input.nextLine();

        System.out.println("\n--- Dados do Professor ---");
        System.out.println("Nome: " + nome);
        System.out.println("Data de Nascimento: " + dataNascimento);
        System.out.println("Endereço: " + endereco);
        System.out.println("Gênero: " + genero);

        input.close();
    }
}
```
# CODIGO PARA CADASTRO DE PESSOA FISICA
```java
import java.util.Scanner;

public class CadastroPessoaFisica {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Digite o nome completo: ");
        String nome = input.nextLine();

        System.out.print("Digite o CPF: ");
        String cpf = input.nextLine();

        System.out.print("Digite a data de nascimento (dd/mm/aaaa): ");
        String dataNascimento = input.nextLine();

        System.out.print("Digite o endereço completo: ");
        String endereco = input.nextLine();

        System.out.print("Digite o gênero: ");
        String genero = input.nextLine();

        System.out.println("\n--- Dados da Pessoa Física ---");
        System.out.println("Nome Completo: " + nome);
        System.out.println("CPF: " + cpf);
        System.out.println("Data de Nascimento: " + dataNascimento);
        System.out.println("Endereço Completo: " + endereco);
        System.out.println("Gênero: " + genero);

        input.close();
    }
}
```
# CODIGO PARA CADASTRO DE PESSOA JURIDICA 
'''JAVA
import java.util.Scanner;

public class CadastroPessoaJuridica {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Digite a razão social: ");
        String razaoSocial = input.nextLine();

        System.out.print("Digite o CNPJ: ");
        String cnpj = input.nextLine();

        System.out.print("Digite o endereço completo: ");
        String endereco = input.nextLine();

        System.out.print("Digite o telefone: ");
        String telefone = input.nextLine();

        System.out.println("\n--- Dados da Pessoa Jurídica ---");
        System.out.println("Razão Social: " + razaoSocial);
        System.out.println("CNPJ: " + cnpj);
        System.out.println("Endereço Completo: " + endereco);
        System.out.println("Telefone: " + telefone);

        input.close();
    }
}
```
# CODIGO PARA CADASTRO DE FORNECEDOR
```java
import java.util.ArrayList;
import java.util.Scanner;

public class CadastroFornecedor {
    ArrayList<String> cadastroFornecedor = new ArrayList<>();
    private String nome;
    private String endereco;
    private String telefone;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        cadastroFornecedor.add(nome);
        this.nome = nome;
    }

    public String getEndereco() {
        return endereco;
    }

    public void setEndereco(String endereco) {
        cadastroFornecedor.add(endereco);
        this.endereco = endereco;
    }

    public String getTelefone() {
        return telefone;
    }

    public void setTelefone(String telefone) {
        cadastroFornecedor.add(telefone);
        this.telefone = telefone;
    }

    public static void main(String[] args) {
        Scanner dados = new Scanner(System.in);
        Scanner dados1 = new Scanner(System.in);
        Scanner dados2 = new Scanner(System.in);

        CadastroFornecedor c1 = new CadastroFornecedor();

        String nome = "";
        String endereco = "";
        String telefone = "";

        System.out.println("Opções\n 1-Cadastrar fornecedor\n 2-Remover fornecedor\n 3-Verificar fornecedor\n");

        int numopc = 0;
        System.out.print("nº: ");
        numopc = dados.nextInt();

        while (numopc == 1) {
            switch (numopc) {
                case 1:
                    System.out.println("Nome do fornecedor: ");
                    nome = dados1.nextLine();
                    c1.setNome(nome);

                    System.out.println("Endereço do fornecedor: ");
                    endereco = dados2.nextLine();
                    c1.setEndereco(endereco);

                    System.out.println("Telefone do fornecedor: ");
                    telefone = dados.nextLine();
                    c1.setTelefone(telefone);

                    System.out.println("\nCadastrar mais fornecedores?\n 1-Sim\n 0-Não\n");
                    numopc = dados.nextInt();
                    break;

                case 2:
                    break;
            }
        }
        
        System.out.println(c1.cadastroFornecedor.toString());
    }
   
}

```

# AUTOR 

Renan Gonçalves Dos Santos
