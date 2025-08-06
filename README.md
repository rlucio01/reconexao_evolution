# 📱 Evolution WhatsApp Reconnect

Página HTML standalone para reconexão de instâncias WhatsApp via Evolution API. Interface responsiva com QR Code auto-refresh e configuração via URL parameters.

## ✨ Características

- 🔗 **Standalone** - Apenas 1 arquivo HTML, sem dependências
- 🔄 **Auto-refresh** - QR Code se renova automaticamente a cada 30s
- 🔐 **Configuração segura** - Credenciais via URL parameters (Base64)
- 📱 **Responsivo** - Funciona em mobile e desktop
- ⚡ **Detecção automática** - Identifica quando WhatsApp conectou
- 🎯 **Feedback inteligente** - Diferentes status de conexão
- 🛠️ **Teste integrado** - Validação de credenciais antes de gerar link

## 🚀 Como Usar

### 1. Para Desenvolvedores/Suporte

1. Abra o arquivo `reconexao-evolution.html` no navegador
2. Preencha os campos:
   - **URL Base da API**: `https://sua-api.com`
   - **API Key**: Sua chave de API Evolution
   - **Nome da Instância**: Nome da instância WhatsApp
3. Clique em **"🧪 Testar Conexão"** para validar (opcional)
4. Clique em **"🔗 Gerar Link para Cliente"**
5. Copie o link gerado e envie para o cliente

### 2. Para Clientes Finais

1. Clique no link recebido
2. Escaneie o QR Code com WhatsApp
3. Aguarde a confirmação de conexão

## 📋 Status de Conexão

| Status | Descrição | Ação |
|--------|-----------|------|
| 🟢 **Conectada** | WhatsApp já conectado | Nenhuma ação necessária |
| 🟡 **Pronta para conexão** | Aguardando scan do QR | Escanear QR Code |
| 🔴 **Desconectada** | WhatsApp desconectado | Reconectar via QR |

## 🔧 Tratamento de Erros

- **Status 401**: API Key incorreta
- **Status 404**: Nome da instância não encontrado  
- **Outros erros**: Verificar credenciais
- **Erro de rede**: Verificar URL da API

## 💡 Exemplo de URL Gerada

```
reconexao-evolution.html?config=eyJhcGlCYXNlVXJsIjoi...
```

A configuração é codificada em Base64 para ofuscar as credenciais na URL.

## 🔒 Segurança

- Credenciais não ficam hardcoded no arquivo
- Encoding Base64 ofusca informações na URL
- Cada link é único para uma instância específica
- Sem persistência de dados no cliente

## 📱 Interface

### Tela de Configuração (Desenvolvedor)
- Formulário para inserir credenciais
- Botão de teste de conexão
- Gerador de link personalizado

### Tela de Scanner (Cliente)
- QR Code responsivo
- Timer de auto-refresh
- Status de conexão em tempo real
- Feedback visual de sucesso

## 🛠️ Compatibilidade

- ✅ Evolution API v2.x
- ✅ Todos navegadores modernos
- ✅ Mobile e desktop
- ✅ Sem dependências externas

## 📄 Licença

MIT License - Use livremente em seus projetos!

---

**Criado com ❤️ para facilitar reconexões WhatsApp via Evolution API**
