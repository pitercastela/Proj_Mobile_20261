# Morador

- **Funcionalidade**: Reservar um espaço comum
    
    **Como**: Um morador do condomínio
    
    **Eu quero**: Reservar uma quadra comum
    
    **Para**: Usar a quadra durante o dia
    
    **Cenário** : Tentativa de reserva
    
    **Dado** que estou logado no sistema
    
    **E** estou em dia com as tachas do condomínio
    
    **Quando** Selecionar o espaço comum com a data/horário
    
    **Então** Vejo uma mensagem de confirmação
    
- **Funcionalidade**: Visualização de Inadimplência
    
    **Como** um morador
    
    **Eu quero** ser notificado automaticamente se estiver inadimplente ao tentar fazer uma reserva
    
    **Para** regularizar minha situação antes de prosseguir
    
    **Cenário**: Tentativa de reserva com pendência
    
    **Dado** que estou logado no sistema
    
    **E** estou com alguma taxa em atraso
    
    **Quando** eu tentar selecionar um espaço e horário
    
    **Então** o sistema bloqueia a reserva
    
    **E** exibe uma mensagem clara: "Você possui pendências financeiras. Regularize para fazer novas reservas."
    
- **Funcionalidade**: Escolha do Espaço
    
    **Como** um morador
    
    **Eu quero** visualizar uma lista com fotos e descrições de todos os espaços disponíveis (salão de festas, quadra, brinquedoteca)
    
    **Para** escolher o local que melhor atende à minha necessidade
    
    **Cenário**: Listagem de espaços
    
    **Dado** que estou na tela inicial do aplicativo
    
    **Quando** eu acessar a opção "Reservar Espaço"
    
    **Então** vejo uma lista de todos os espaços comuns
    
    **E** cada espaço tem uma foto e nome
    
- **Funcionalidade**: Filtro de Disponibilidade
    
    **Como** um morador
    
    **Eu quero** ver um calendário interativo mostrando apenas os dias e horários livres para o espaço escolhido
    
    **Para** não perder tempo tentando reservar um horário já ocupado
    
    **Cenário**: Visualização de horários livres
    
    **Dado** que selecionei a "Quadra Poliesportiva"
    
    **Quando** eu abrir o calendário
    
    **Então** os dias com horários disponíveis aparecem destacados (ex: em verde)
    
    **E** os dias lotados aparecem cinzas e bloqueados para seleção
    
- **Funcionalidade**: Conflito de Horários
    
    **Como** um morador
    
    **Eu quero** ser avisado imediatamente se o horário que tentei reservar for ocupado por outro morador enquanto eu preenchia os dados
    
    **Para** escolher outro horário sem frustração
    
    **Cenário**: Horário perdido durante o preenchimento
    
    **Dado** que estou preenchendo os detalhes da reserva
    
    **Quando** eu clicar em "Confirmar"
    
    **E** o horário foi reservado por outro usuário nos últimos minutos
    
    **Então** recebo uma mensagem: "Horário indisponível. Por favor, escolha outro."
    
    **E** o calendário é atualizado com a nova ocupação
    
- **Funcionalidade**: Lembrete Automático
    
    **Como** um morador que fez uma reserva
    
    **Eu quero** receber uma notificação push 1 hora antes do início da minha reserva
    
    **Para** não esquecer o compromisso e me programar para chegar no horário
    
    **Cenário**: Lembrete próximo ao evento
    
    **Dado** que reservei a churrasqueira para as 18h
    
    **Quando** o relógio marcar 17h do dia da reserva
    
    **Então** recebo uma mensagem: "Lembrete: Sua reserva da Churrasqueira começa em 1 hora."
    
- **Funcionalidade**: Aviso de Ocupação
    
    **Como** um morador
    
    **Eu quero** ser avisado se um espaço que eu reservei, for bloqueado para algum evento do condomínio
    
    **Para** que eu possa agendar outro horário
    
    **Dado** que fiz uma reserva para o salão de festas no próximo sábado
    
    **E** a administração do condomínio precisa utilizar o espaço para uma assembleia geral no mesmo dia e horário
    
    **Quando** o administrador realizar o bloqueio do espaço no sistema
    
    **Então** recebo uma notificação imediata informando: "Sua reserva do Salão de Festas para [data/horário] precisou ser cancelada devido a um evento do condomínio"
    
    **E** a notificação inclui um link para "Ver horários alternativos disponíveis"
    
    **E** meu histórico de reservas mostra o status como "Cancelado pelo condomínio"
    

# Administrador

- **Funcionalidade**: Gestão de Regras por Espaço
    
    **Como** um síndico ou administrador
    
    **Eu quero** definir regras específicas para cada espaço
    
    **Para** que o uso seja organizado e justo para todos
    
    **Cenário**: Configuração de espaço
    
    **Dado** que estou logado como administrador
    
    **Quando** eu acessar a configuração de um espaço comum
    
    **Então** posso definir campos como: "Antecedência máxima para reserva (dias)" e "Limite de reservas por mês por morador"
    
- **Funcionalidade**: Bloqueio de Agenda
    
    **Como** um administrador
    
    **Eu quero** bloquear determinados dias e horários no calendário coletivo
    
    **Para** realizar manutenções ou eventos privativos do condomínio sem conflitos com reservas de moradores
    
    **Cenário**: Bloqueio para manutenção
    
    **Dado** que a quadra passará por manutenção na segunda-feira
    
    **Quando** eu acessar o calendário da quadra como admin
    
    **E** selecionar "Bloquear período"
    
    **Então** a segunda-feira inteira fica indisponível para todos os moradores
    
    **E** uma notificação é enviada avisando sobre a manutenção
