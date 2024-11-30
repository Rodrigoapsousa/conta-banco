## Getting Started

Esse foi um pouco do meu esforço em aprender java.
import java.util.Scanner;  // Importando a classe Scanner para entrada de dados

public class ContaTerminal {

    // 1. Declaração dos atributos da classe sem static
    int numero;
    String agencia;
    String nomeCliente;
    double saldo;

    public static void main(String[] args) {
        // 2. Criação do objeto Scanner para capturar dados do usuário
        Scanner scanner = new Scanner(System.in);

        // 3. Criar uma instância de ContaTerminal para acessar as variáveis não estáticas
        ContaTerminal conta = new ContaTerminal();

        // 4. Exibir mensagens para o usuário
        System.out.println("Por favor, digite o número da Conta:");
        conta.numero = scanner.nextInt();  // Acessando a variável 'numero' da instância 'conta'

        scanner.nextLine();  // Consumir a quebra de linha após nextInt() para usar nextLine() depois

        System.out.println("Por favor, digite o número da Agência:");
        conta.agencia = scanner.nextLine();  // Acessando a variável 'agencia' da instância 'conta'

        System.out.println("Por favor, digite o nome do Cliente:");
        conta.nomeCliente = scanner.nextLine();  // Acessando a variável 'nomeCliente' da instância 'conta'

        System.out.println("Por favor, digite o saldo da Conta:");
        conta.saldo = scanner.nextDouble();  // Acessando a variável 'saldo' da instância 'conta'

        // 5. Exibir a mensagem final com os dados coletados
        System.out.println("Olá " + conta.nomeCliente + ", obrigado por criar uma conta em nosso banco, sua agência é " +
                conta.agencia + ", conta " + conta.numero + " e seu saldo " + conta.saldo + " já está disponível para saque.");

        // Fechar o scanner
        scanner.close();  
    }
}

## Folder Structure

The workspace contains two folders by default, where:

- `src`: the folder to maintain sources
- `lib`: the folder to maintain dependencies

Meanwhile, the compiled output files will be generated in the `bin` folder by default.

> If you want to customize the folder structure, open `.vscode/settings.json` and update the related settings there.

## Dependency Management

The `JAVA PROJECTS` view allows you to manage your dependencies. More details can be found [here](https://github.com/microsoft/vscode-java-dependency#manage-dependencies).
