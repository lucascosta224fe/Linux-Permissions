# Linux-Permissions
Gerenciando permissões no Linux

<h2>📁Project description</h2>

Neste projeto o objetivo é gerenciar corretamente as permissões em linux demonstrando domínio e capacidade de análise sobre o que aparece na tela.

Foi dado diretórios com permissões incorretas e cabe a mim resolvê-las.

Deve-se seguir os seguintes tópicos:

A organização não permite que outras pessoas tenham acesso de gravação a nenhum arquivo.

A equipe de pesquisa arquivou o arquivo `.project_x.txt`, e é por isso que ele é um arquivo
oculto. Esse arquivo não deve ter permissões de gravação para ninguém, mas o usuário e o
grupo devem ser capazes de ler o arquivo. Use um comando do Linux para atribuir a
`.project_x.txt` a autorização apropriada.

Os arquivos e diretórios no diretório projects pertencem ao usuário `researcher2`. Somente o
`researcher2` deve ter permissão para acessar o diretório `drafts` e seu conteúdo. Use um
comando do Linux para modificar as permissões adequadamente.

<h2>🗂Check file and directory details </h2>

![image](https://github.com/user-attachments/assets/914d0979-4e06-402d-b39b-8bb88d329dc9)

Primeiro uso um `ls - la` para verificar todas as permissões, incluindo também a de arquivos
escondidos para verificar o que está de acordo com o enunciado e o que não está.

<h2> 🖋 Describe the permissions string </h2>

Na string de caracteres temos 10 letras ou hifens.
O primeiro “d” ou “-” representa o tipo de dado que estamos usando, “d” é para diretório e “-”
é para arquivo.

Vou utilizar como exemplo a linha abaixo de “total 32
”
Em seguida do 2 caractere até o 4 “rwx” significa que é o usuário, que tem todas as
permissões. O “r” significa read, “w” write e “x” execute.

Do 5 caractere até o 7 “r-x” significa que é o grupo, tem somente a função de ler e de executar
o arquivo/diretório.

Do 8 caractere até o 10 “r-x” significa que são “outros” e que tem permissões para ler e
executar também.

<h2>💾Change file permissions</h2>

![image](https://github.com/user-attachments/assets/a2bf808a-3be7-4ab5-a6f5-185aa0a935a6)

á que a organização não permite que outras pessoas tenham acesso a gravação dos arquivos eu retirei a permissão de gravação do único arquivo que não estava de acordo. Utilizei o `chmod` que altera as permissões dos usuários, grupo e outros onde recebe o parâmetro do que deve ser mudado e do diretório/arquivo

<h2>🔒Change file permissions on a hidden file</h2>

![image](https://github.com/user-attachments/assets/3f7eab3b-bf1e-4ac9-8ab7-6c6510885382)

Já que ninguém pode escrever no arquivo escondido eu alterei as permissões para grupo e usuário tirando a opção de escrever e adicionando a de ler no grupo. Dava pra utilizar da vírgula mais uma vez na primeira linha, mas por questões de deixar mais claro optei por deixar a 2 linha como adicionar permissões e a primeira como retirar permissões

<h2>📲Change directory permissions</h2>

![image](https://github.com/user-attachments/assets/0f96214a-d7c7-4c2d-867d-8ab5419fb972)

O diretório drafts só pode ser acessado pelo usuário então o grupo não poderia executá-lo,
logo tirei a função x dele

<h2>📕Summary</h2>

Basicamente nesse documento realizei a modificação de permissões de arquivos normais e escondidos com o chmod e analisei quais as permissões que cada um tinha no sistema com o ls -la mostrando todos os arquivos para uma fácil compreensão do que faltava.

