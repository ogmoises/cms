# CMS - Criação de conteúdo

## Blocos

<div style="text-align: justify; margin-bottom: 1em;">
No contexto das plataformas de gestão de conteúdo (CMS), o conceito de blocos é central na construção de páginas e posts. Blocos são componentes que permitem a criação de layouts dinâmicos sem a necessidade de programação direta. Podem ser parágrafos, imagens, galerias, vídeos, botões ou códigos embutidos. Seu objetivo principal é facilitar o processo de criação de conteúdo.
</div>

## Criação de Blocos

<div style="text-align: justify; margin-bottom: 1em;">
Processo de desenvolvimento de novos blocos ou componentes. A criação de blocos envolve codificar e estruturar blocos personalizados que podem ser adicionados ao editor e usados repetidamente. Esta parte do processo geralmente é feita por desenvolvedores, usando ferramentas como React, JavaScript, HTML, e CSS.
</div>
<div style="text-align: justify; margin-bottom: 1em;">
Utilizando da criação de blocos, podemos configurar blocos com funções específicas, como galerias de imagens, carrinhos de compras, formulários de contato e até mesmo blocos de texto com estilos restritos ou específicos.
</div>

## Edição de Blocos

<div style="text-align: justify; margin-bottom: 1em;">
Ajuste do conteúdo de páginas ou posts, utilizando como base os blocos já criados. Esta parte da criação de conteúdo não necessita profundo conhecimento técnico e é feita pelos usuários finais. Nela, é possível adicionar, remover e reorganizar blocos, bem como editar o conteúdo dentro de cada um deles.
</div>
<div style="text-align: justify; margin-bottom: 1em;">
Algumas das tarefas competentes aos editores de blocos são: a inserção de parágrafos e modificações de texto, a alteração das propriedades como tamanho e alinhamento de um bloco de imagem e adição de blocos de vídeo, bem como o ajuste de sua posição na página.
</div>

## Criação de Blocos no WordPress

<div style="text-align: justify; margin-bottom: 1em;">
Em WordPress, utilizamos o editor de blocos Gutenberg. Este editor utiliza o React para renderizar a interface de usuário dos blocos, permitindo com que componentes modulares que se encaixam na estrutura dos blocos possam ser criados. Como o WordPress é baseado em PHP, o backend de um bloco muitas vezes depende dessa linguagem de programação para registrar blocos e lidar com o processamento no servidor. Outras linguagens como HTML e CSS podem ser utilizadas a fim de definir a estrutura e o estilo de conteúdo dos blocos.
</div>

<div style="text-align: justify; margin-bottom: 1em;">
A partir dessas tecnologias, é possível desenvolver blocos reutilizáveis, além de funcionalidades e personalizações que podem ser adicionadas ao editor.
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Ao criar um bloco, seu comportamento e propriedades devem ser definidos tanto no frontend quanto no backend. Sua estrutura básica é definida no JavaScript e pode ser registrada utilizando a função registerBlockType.  Para criar blocos dinâmicos, utilizaremos register_block_type, no lado do servidor do PHP.
</div>

## Ciclo de Vida de um Bloco

<div style="text-align: justify; margin-bottom: 1em;">
Registro: Como já apresentado, a função registerBlockType será utilizada a fim de registrar o bloco. Nessa etapa, definiremos as propriedades do bloco (título, categoria, ícone, …). Este processo identifica como o bloco será tratado no editor. O código a seguir cria um bloco simples com um campo de texto editável. code
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Edição: Essa função define como o bloco será exibido e editado. Esse é o ponto em que o usuário interage com o bloco. code
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Atributos: Dados armazenados pelo bloco. Salvam seu conteúdo e são atualizados conforme as interações do usuário com o mesmo. code
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Salvamento: Define como o conteúdo será salvo no banco de dados. Utiliza os atributos definidos na função de edição e gera a marcação a ser exibida. code
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Por fim, o conteúdo publicado é renderizado no frontend do site.
</div>

## Posts

<div style="text-align: justify; margin-bottom: 1em;">
Geralmente utilizados para conteúdo dinâmico. Tem como principal característica a organização cronológica inversa dos conteúdos (postagens mais recentes no topo das listagens). São exemplos de posts: artigos, notícias e conteúdos de blogs. São ideais para sites cuja atualização frequente do conteúdo é essencial.
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Além disso, os posts permitem comentários de usuários e utilizam categorias e tags, o que facilita sua organização e navegação pelos visitantes. Estes também estão diretamente conectados aos feeds RSS, permitindo que os leitores assinem as atualizações do site, para que seja possível receber novos conteúdos de maneira automática. Devido a essas características, são amplamente utilizados para gerar tráfego e manter usuários engajados.
</div>

## Páginas

<div style="text-align: justify; margin-bottom: 1em;">
Geralmente utilizadas para conteúdo estático. São utilizadas para informações permanentes e estruturais de um site. São exemplos de páginas: abas de contato e serviços do site.
</div>

<div style="text-align: justify; margin-bottom: 1em;">
Diferentemente de posts, as páginas não estão vinculadas a uma linha do tempo cronológica, não sendo organizadas por data ou categorias. Normalmente, não são incluídas nos feeds RSS, uma vez que seu conteúdo não precisa ser atualizado regularmente. Além disso, podem ser organizadas de forma hierárquica, o que significa que há a possibilidade de haver subpáginas relacionadas, facilitando a criação de uma estrutura de navegação complexa e organizada dentro do site.
</div>
