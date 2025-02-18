## Cenário 4 

Aqui estão alguns casos de teste para validar a entrada de dados nos campos modificados:  

---

###  Nome Completo 
 **Cenários de teste válidos**:  
- Inserir um nome completo com letras e espaços (ex: "Maria Eduarda Müller Ermes")  
- Inserir um nome com caracteres acentuados (ex: "Érika Souza")  

 **nomes inválidos**:  
- Inserir apenas um nome (ex: "Carlos")  
- Inserir números no nome (ex: "Maria123")  
- Inserir caracteres especiais não permitidos (ex: "José@Silva")  
- Campo vazio  

---

###  E-mail  
 **Cenários de teste válidos**:  
- E-mail com formato correto (ex: "usuario@dominio.com")  
- E-mail com subdomínio (ex: "usuario@sub.dominio.com")  

 **E-mails inválidos**:  
- E-mail sem "@" (ex: "usuariodominio.com")  
- E-mail sem domínio (ex: "usuario@.com")  
- E-mail com espaços (ex: "usuario @dominio.com")  
- E-mail com caracteres especiais não permitidos (ex: "usuário!@dominio.com")  
- Campo vazio  

---

### Número de telefone
 **Cenários de teste válidos**:  
- Formato nacional (ex: "(11) 91234-5678")  
- Formato internacional (ex: "+55 11 91234-5678")  

**Números inválidos**:  
- Número com menos de 10 dígitos (ex: "9123-567")  
- Número com caracteres alfabéticos (ex: "abc12345678")  
- Número sem DDD onde for obrigatório (ex: "91234-5678")  
- Número com caracteres especiais extras (ex: "11@91234-5678")  
- Campo vazio  

---

###  Data de nascimento
**Cenários de teste válidos**:  
- Data no formato correto (ex: "15/08/1990" ou "1990-08-15")  
- Data com idade maior que 18 anos  

 **Datas inválidas**:  
- Data no formato incorreto (ex: "15-08-1990", "1990/08/15")  
- Data futura (ex: "10/10/2030")  
- Usuário menor de idade (ex: "15/08/2015")  
- Caracteres inválidos no campo (ex: "abcd-ef-gh")  
- Campo vazio  

---

### Endereço

####  Rua  
 **Cenários de teste válidos**:  
- Nome da rua com letras e números (ex: "Rua das Flores, 123")  

 **Ruas inválidas**:  
- Nome da rua com caracteres especiais inválidos (ex: "Rua $$%%")  
- Campo vazio  

#### Cidade 
 **Cenários de teste válidos**:  
- Nome da cidade apenas com letras (ex: "São Paulo")  

 **Cidades inválidas**:  
- Cidade com números ou caracteres especiais inválidos (ex: "S@o Paulo123")  
- Campo vazio  

#### **Estado**  
 **Cenários de teste válidos**:  
- Sigla do estado correta (ex: "SP", "RJ")  

**Estados inválidos**:  
- Nome completo do estado ao invés da sigla (ex: "São Paulo" em vez de "SP")  
- Sigla com mais de dois caracteres (ex: "SPP")  
- Campo vazio  

#### CEP 
**Cenários de teste válidos**:  
- CEP com formato correto (ex: "12345-678")  

 **CEPs inválidos**:  
- CEP com menos dígitos (ex: "1234-678")  
- CEP com letras (ex: "12A45-6B8")  
- CEP com caracteres especiais extras (ex: "12345/678")  
- Campo vazio  