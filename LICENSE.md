#alunas: giovanna oliveira de souza e maria vitória das neves rabelo
class Supermercado:
    ##construtor
    def _init_(self, numeroProdutos):
        self.__numeroProdutos = numeroProdutos
## os métodos de acesso (get e set) para o atributo numeroProdutos.
    def get_numeroProdutos(self):
        return self.__numeroProdutos

    def set_numeroProdutos(self, numeroProdutos):
        self.__numeroProdutos = numeroProdutos

    def calcularTotal(self):
        total = 0
        for i in range(self.__numeroProdutos):
            valor = float(input(f"Digite o valor do produto {i+1}: "))
            total += valor
        print("O valor total das compras no supermercado é:", total)

class TestarSupermercado:
    def main():
        num_produtos = int(input("Digite o número de produtos: "))
        supermercado = Supermercado(num_produtos)
        supermercado.calcularTotal()
        novo_numero_produtos = int(input("Digite o novo número de produtos: "))
        supermercado.set_numeroProdutos(novo_numero_produtos)
        supermercado.calcularTotal()
if _name_ == "_main_":
    TestarSupermercado.main()
