# lista-de-exercicios

Thiago de Oliveira Paravati RA: 125111352704
Vinicius Moraes Teixeira RA: 12511121327314
 
Resposta dos Exercicios

1)	GLSL significa OpenGL Shader Language, que seria um tipo de linguagem de shader no opengl e são lá em que os shaders são escritos. Os shaders obrigatórios seriam o vertex shader e o fragment shader.

-	Vertex shader: ele processa a posição 3D -> 2D, recebe como entrada um único vértice. O principal objetivo do vertex shader é transformar as coordenadas 3D em diferentes coordenadas 3D. Vertex shader nos permite fazer algum processamento básico nos atributos do vértice. Responsável por tratar um vértice pelas coordenadas de textura, posicionar os vértices nas coordenadas finais, recebe as posições dos vértices e joga na saída e processa também sua cor.

-	Fragment shader: Após o processamento final do vertex shader fragmente shader fica responsável por tratar os fragmentos entre os verticies (fragmento, todos os dados necessários para o OpenGL renderizar um único pixel). Seu objetivo é calcular a cor final de um pixel e este é geralmente o estágio onde ocorrem todos os efeitos avançados do OpenGL. Normalmente, o sombreador de fragmento contém dados sobre a cena 3D que ele pode usar para calcular a cor final do pixel (como luzes, sombras, cor da luz e assim por diante). Uma área pixel-size, cor de cada fragmento, zdapth e alpha value.

2)	As primitivas são os elementos gráficos mais simples que podem ser criados dentro de uma aplicação. A partir dessas primitivas são construídos cenários,
personagens e objetos em uma aplicação de computação gráfica.
A biblioteca suporta primitivas baseadas em pontos e linhas (GL_POINTS, GL_LINES, etc) e primitivas baseadas em faces (GL_QUADS, GL_TRIANGLES, etc). A diferença 
é que por definição, as primitivas baseadas em linhas apenas geram um traçado, enquanto as baseadas em faces apenas PINTAM o conteúdo (não traçam).

3)	VBO - objeto de buffer de vértice, responsável por armazenar em sua memoria os dados dos vértices, pode armazenar um grande número de vértices na memória da GPU. A vantagem de usar esses objetos de buffer é que podemos enviar grandes lotes de dados de uma só vez para a placa gráfica e mantê-los lá se houver memória suficiente, sem ter que enviar dados um vértice de cada vez. O envio de dados para a placa de vídeo a partir da CPU é relativamente lento, portanto, sempre que pudermos, tentamos enviar o máximo de dados possível de uma só vez. Uma vez que os dados estão na memória da placa gráfica, o vertex shader tem acesso quase instantâneo aos vértices tornando-o extremamente rápido.

VAO - Objeto de matriz de vértices, pode ser vinculado como um objeto de buffer de vértice e qualquer chamada de atributo de vértice subsequente a partir desse ponto será armazenada dentro do VAO. Isso tem a vantagem de que ao configurar ponteiros de atributo de vértice você só precisa fazer essas chamadas uma vez e sempre que quisermos desenhar o objeto, podemos apenas vincular o VAO correspondente. Isso torna a alternância entre diferentes dados de vértices e configurações de atributos tão fácil quanto vincular um VAO diferente. Todo o estado que acabamos de definir é armazenado dentro do VAO.

EBO- Objetos de buffer de elemento, 
Um EBO é um buffer, assim como um objeto de buffer de vértice, que armazena índices que o OpenGL usa para decidir quais vértices desenhar. Este assim chamado desenho indexado é exatamente a solução para o nosso problema. Para começar, primeiro temos que especificar os vértices (únicos) e os índices para desenhá-los como um retângulo: ao usar índices, precisamos apenas de 4 vértices em vez de 6. Em seguida, precisamos criar o objeto buffer do elemento.

4) 
