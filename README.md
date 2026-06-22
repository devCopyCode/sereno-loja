# SERENO — Loja de Linho

Site de e-commerce para a marca SERENO, especializada em roupas de linho feitas em São Paulo.

## 🎨 Características

- **Catálogo de Produtos**: 8 itens principais + 3 edições limitadas
- **Carrinho de Compras**: Gerenciamento de itens com quantidade e remoção
- **Checkout Completo**: 
  - 4 métodos de pagamento (Crédito, Débito, PIX, Boleto)
  - Cálculo de frete dinamicamente pelo CEP
  - Dados pessoais e endereço
- **Design Responsivo**: Otimizado para desktop e mobile
- **Sem Backend**: Simulação completa em HTML/CSS/JavaScript puro

## 📁 Estrutura

```
project/
├── SERENO-polished.html      # Site principal
├── SERENO-checkout.html      # Página de checkout
├── imagens/                  # Imagens dos produtos
└── README.md                 # Este arquivo
```

## 🚀 Como Usar Localmente

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/sereno-loja.git
cd sereno-loja
```

2. Abra em um servidor local (Python):
```bash
python -m http.server 8000
```

3. Acesse no navegador:
```
http://localhost:8000/SERENO-polished.html
```

## 💳 Cupons Disponíveis (Checkout)

- `DESCONTO10` → 10% de desconto
- `SERENO20` → 20% de desconto
- `WELCOME5` → 5% de desconto

## 📦 Frete (Cálculo Automático pelo CEP)

- SP Capital (01): R$ 15
- SP Interior (0X): R$ 20
- RJ/Minas (2-3): R$ 35
- Sul (4-5): R$ 45
- Norte/Nordeste (outros): R$ 50

## ⚠️ Informações Importantes

- ❌ Nenhum dado é salvo no servidor
- ❌ Pagamento é simulado
- ✅ Ideal para demonstração e prototipagem

## 🛠️ Tecnologias

- HTML5
- CSS3 (Custom Properties)
- JavaScript (Vanilla)
- IntersectionObserver API para scroll animations

## 📄 Licença

Propriedade da marca SERENO © 2026

---

Desenvolvido com ❤️ para SERENO
