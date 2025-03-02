# TODO

  ## hardware
  CPU Virtual(Registradores, opcodes, tamanho dos dados, tamanho do barramento de dados e endereço),
  como voce vai fazer uma cpu 16 ou 8, seria bom fazer baseada no 8605 (nao lembro o nome, mas ta realacionado com x86)
  Além de criar os registradores flag(interno, o usuario nao vai modificar diretamente.

  Memoria RAM
  Depende muito da cpu, a cpu tem que ter um barramento de endereco de memoria de 16 para 65536 enderecos e 2 registradores para 
  fazer algo semelhante, seria MOV $(D+F), 1 onde D e F são registradores que têm seu uso voltado para endereçamento.
  LRDR: colocar

  Caso tenha 8, seria 255 enderecos, o que é muito pouco, nao daria para a memoria ram tankar isso tudo, alem do mais,
  so poderia ter 255 caracteres registrados, a nao ser que use a GPU em conjunto com a CPU

  VRAM
  GPU Virtual
  
  Timer(contador de cloks)

## software

  ### kernel
  Essa parte precisa ser pensada bem, pois existem varios tipos de design de kernel, e o modo que ele age
  Caso esteja interessado em fazer uma pesquisa antecipada: unikernel, nanokernel, exokernel,  microkernel, monolitico

  Mas em geral, tem essas partes:
    - Gerenciamento de Memoria
    - Gerenciamento de processos
    - Sicronização e demais relacionados a eventos baseados em tempo
    - manipulador de entrada
    - VFS(Virtual FileSystem)
    - API lowlevel
    - (Caso queira)Memoria Virtual(avancado) Isso pode ser implementado posteriormente
          
  ### OS
  Pode ser fortemente baseado no MSDOS, se quiser dá para fazer cross-compilation para executar ele no kernel(porem

  Caso o fantasy terminal seja um pouco mais além
            - Program loader
            - UI(personalizavel?)
            - default applications(nao, isso será necessario)
            - Package manager(caso queira fazer alguma conexao web para fazer a requisicao de apps, etc)
            - Depurador(muito bom)
            

  Nós podemos criar uo nosso proprio .exe ou .com(arquivo executavel do MSDOS), drivers, uma linguagem de script como powershell ou batch
