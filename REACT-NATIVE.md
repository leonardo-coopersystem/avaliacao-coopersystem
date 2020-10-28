


# Projeto de seleção Coopersystem (React Native)
  
O teste consiste em criar uma mini aplicação que react native que simula um resgate personalizado de fundos de investimentos em ações.  
  
Serão avaliados:  
* Integração com api rest
* Navegação entre telas  
* Validação de formulários conforme regras de negócios  
* Padrões de codificação  
* Testes unitários ( jest js )  
	
 
**Obs:** Os layouts dos protótipos são só ilustrativos, podem usar os frameworks de ux/estilo de sua preferência.
  
### Protótipos  
* React Native  
	* [Lista de investimentos](https://github.com/leonardo-coopersystem/avaliacao-coopersystem/blob/master/prototipos-react-native/1%20-%20Lista%20de%20investimentos.png?raw=true)  
	* [Resgate personalizado](https://github.com/leonardo-coopersystem/avaliacao-coopersystem/blob/master/prototipos-react-native/2%20-%20Simula%C3%A7%C3%A3o%20do%20resgate.png?raw=true)  
	* [Modal de confirmação](https://github.com/leonardo-coopersystem/avaliacao-coopersystem/blob/master/prototipos-react-native/3%20-%20Confirma%C3%A7%C3%A3o.png?raw=true)
  
  
### Fluxo de navegação  
* Lista de investimentos  
	* Executar uma chamada get no endereço [http://www.mocky.io/v2/5e76797e2f0000f057986099](http://www.mocky.io/v2/5e76797e2f0000f057986099)
	* Montar a  tela conforme o protótipo fazendo a integração com serviço acima.
	* Ao clicar em um plano que não esta em carência (indicadorCarencia = 'N'), navegar para próxima tela. 
*  Resgate personalizado  
	 * Montar a  tela conforme o protótipo usando as informações do fundo de investimento selecionado na tela anterior.
	 * Digitar os valores que deseja resgatar de cada ação e clicar em confirmar resgate
* Modal de confirmação
	* Montar a  tela conforme o protótipo.

### Regras de Negocio  
* Tela 1: Lista de investimentos  
	* Fundos de investimentos em carência (indicadorCarencia = 'S') não pode realizar resgate, deve ficar desabilitado na lista de investimentos.  
  
* Resgate personalizado  
	* Valor a resgatar de cada ação não pode ser maior que saldo acumulado da mesma, deve ser exibido um alerta para cliente quando isso acontecer.  
	* A cada interação, deve ser atualizado o valor total a resgatar.  
	* Valor total a resgatar não pode ser maior que valor total disponível, deve ser exibido um alerta para cliente quando isso acontecer.  
	* Ao clicar no botão de confirmar, alem de validar as regras acimas, deve validar se o valor total a resgatar não e igual a 0, caso o contrario, deve exibir um alerta ao cliente para preencher os valores a resgatar da forma que ele deseja.  
	* Após todas a validações deve abrir o modal de resgate efetuado.

### Entrega
Enviar link do git com os testes para o email
leonardo.guedes@coopersystem.com.br

### Telefone para duvidas
61 9 8194-1274

### JSON

Caso o link do json não estiver disponível, pode usar este site para criar um novo endpoint

[https://www.mocky.io/](https://www.mocky.io/)

    {
	  "response": {
	    "status": "200",
	    "data": {
	      "listaInvestimentos": [
	        {
	          "nome": "INVESTIMENTO I",
	          "objetivo": "Minha aposentadoria",
	          "saldoTotalDisponivel": 39321.29,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 28.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 20.71
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 21.63
	            },
	            {
	              "id": "4",
	              "nome": "CMIG3",
	              "percentual": 12.41
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 17.15
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO II",
	          "objetivo": "Viajem dos sonhos",
	          "saldoTotalDisponivel": 7300,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 35.81
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 26.42
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 37.77
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO III",
	          "objetivo": "Abrir meu próprio negócio",
	          "saldoTotalDisponivel": 26000,
	          "indicadorCarencia": "N",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 41.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 22.43
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 26.12
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 10.35
	            }
	          ]
	        },
	        {
	          "nome": "INVESTIMENTO IV",
	          "objetivo": "Investimento em carencia",
	          "saldoTotalDisponivel": 44000,
	          "indicadorCarencia": "S",
	          "acoes": [
	            {
	              "id": "1",
	              "nome": "BBAS3",
	              "percentual": 41.1
	            },
	            {
	              "id": "2",
	              "nome": "VALE3",
	              "percentual": 22.43
	            },
	            {
	              "id": "3",
	              "nome": "PETR4",
	              "percentual": 26.12
	            },
	            {
	              "id": "5",
	              "nome": "OIBR3",
	              "percentual": 10.35
	            }
	          ]
	        }
	      ]
	    }
	  }
	}

### BOA SORTE! =)