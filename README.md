# unbbayesandroid

O projeto é uma adaptação do UnBBayes para ser utilizado como biblioteca em projetos Android. 

Para poder utilizar o UnbBayes na plataforma Android como uma biblioteca, foi necessário realizar algumas adaptações, uma vez que a API do Android, apesar de ser baseada em Java, não processa as classes Java de Interface Gráfica (Java Swing, por exemplo), ou classes que utilizam hardware, uma vez que possui classes específicas. Portanto, foi necessário retirar do projeto essas classes.

Inicialmente, do código fonte do UnBBayes foram retiradas algumas funcionalidades para melhor entender o código, pois é bem extenso. Primeiramente, foram retiradas partes da interface gráfica, como as diversas opções do menu, restando somente o menu para abrir uma RB do arquivo, assim como as chamadas de métodos correspondentes. O passo seguinte foi retirar a funcionalidade de se gerar/carregar diagramas de influência (influence diagrams). Uma vez entendido o código, como próxima etapa optou-se por retirar o restante da interface gráfica, por conter as classes das bibliotecas awt e swing (pacote javax), não compatíveis com a API do Android. 

Pelo mesmo motivo, foi necessário também retirar a funcionalidade de carregamento de plugins. Também foram retiradas a maioria das dependências de classes externas, como aquelas que tratam de logs, pois muitas delas eram incompatíveis com a API do Android. Os seguintes arquivos foram retirados do projeto original: commons-logging-1.0.4.jar, javahelp-2.0.02.jar, jaxme2-rt-0.5.1.jar, jaxmeapi-0.5.1.jar, jpf-1.5.jar, log4j-1.2.17.jar, xalan-2.7.0.jar e xml-apis-1.0.b2.jar.

Para utilizar uma biblioteca Java no Android, com o projeto aberto no Android Studio deve-se clicar em “File”, “Project Structure”, vai abrir uma janela, no item “Modules” clicar em “app”, depois em “Dependencies”. Depois é só clicar no botão “+” e importar um arquivo .jar.
O resultado é um projeto leve, com tamanho de 4,74 MB, e o arquivo JAR com tamanho de 1,87 MB, frente aos 48,5 MB do projeto original. Porém possui um único algoritmo de inferência, o de junção de árvore, além de perder várias funcionalidades.

UnBBayesAppV4.0.rar é a Versão 4.0 do UnbBayes para Android, sendo a mais estável.
O arquivo .jar está pronto para ser utilizado em projetos Android.
