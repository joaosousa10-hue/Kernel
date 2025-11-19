Qual foi a versão do kernel que você compilou, e por que escolheu essa versão?      6.8.0-51-generic escolhi pela melhor performance do sistema.

Que configuração você modificou no menuconfig? Por que fez essa modificação? O que espera que essa modificação altere no comportamento do sistema?    desativei o VFAT (windows-95) fs support, pq eu nao iria usar ele, melhorar e liberar um espaço para melhor perfomance.

Durante a compilação você encontrou algum erro, advertência ou comportamento inesperado? Como resolveu ou o que faria para resolver?   sim, o "make" ele nao rodou até o final e deu o erro. e nao achei jeito nenhum de resolver o erro.

Quais os riscos e benefícios de “rodar” um kernel compilado por você mesmo em comparação com usar o kernel padrão da distribuição?     beneficios; remover drivers que não usa,   ativar só o que realmente importa,   otimizar para sua CPU específica.  desvantagens: O sistema pode não iniciar, Segurança depende de você, Perda de compatibilidade, Mais difícil de depurar

Em quais cenários você considera “vale a pena” compilar seu próprio kernel? Cite ao menos dois.      para deixar do jeito que o usuario quiser e personalizar.  mais transparencia e pode compilar para algo expecifico que vc quiser.

Se o sistema não inicializar após a compilação/instalação do kernel, qual seria seu plano de contingência para recuperar o sistema?     Se depois de instalar o kernel novo o sistema não iniciar, eu usaria o GRUB pra selecionar o kernel antigo e entrar normalmente. A partir disso eu removeria o kernel que deu problema e atualizaria o GRUB. Se nem isso funcionasse, eu iniciaria com um Live USB, montaria a partição do sistema e usaria o chroot pra reinstalar um kernel estável. Assim eu consigo recuperar o sistema sem perder nada.
