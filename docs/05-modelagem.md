# Modelagem de Dados



## Entidades

### Morador

- id
- nome
- telefone
- recebe_notificacao
- apartamento_id

### Apartamento

- id
- numero
- bloco

### Porteiro

- id
- nome

### Encomenda

- id
- empresa
- tipo
- codigo
- observacao
- status
- data_registro
- data_entrega
- apartamento_id
- morador_id (opcional)
- porteiro_registro_id
- porteiro_entrega_id



## Relacionamentos

### Apartamento → Morador (1:N)

Um apartamento pode possuir vários moradores.

Um morador pertence a apenas um apartamento.

---

### Apartamento → Encomenda (1:N)

Um apartamento pode receber várias encomendas.

Uma encomenda pertence a um único apartamento.

---

### Morador → Encomenda (1:N)

Um morador pode receber várias encomendas.

Uma encomenda pertence a um único morador quando identificado.

---

### Porteiro → Encomenda (Registro) (1:N)

Um porteiro pode registrar diversas encomendas.

Cada encomenda possui um único porteiro responsável pelo registro.

---

### Porteiro → Encomenda (Entrega) (1:N)

Um porteiro pode entregar diversas encomendas.

Cada encomenda possui um único porteiro responsável pela entrega.



## Observações

- Para o MVP, cada morador pertence a apenas um apartamento.
- O cenário de um morador vinculado a múltiplos apartamentos será avaliado em versões futuras.
- Uma encomenda sempre estará vinculada a um apartamento.
- O vínculo com o morador pode ficar vazio quando não for possível identificá-lo no momento do cadastro.
