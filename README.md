# Fe-ExercicioProposto02.javaSet
Trabalhando com Collections Java Exercícios Propostos Set
## package fe.com;

import java.util.*;

/*
Crie uma conjunto contendo as cores do arco-íris e:
a) Exiba todas as cores o arco-íris uma abaixo da outra;
b) A quantidade de cores que o arco-íris tem;
c) Exiba as cores em ordem alfabética;
d) Exiba as cores na ordem inversa da que foi informada;
e) Exiba todas as cores que começam com a letra ”v”;
f) Remova todas as cores que não começam com a letra “v”;
g) Limpe o conjunto;
h) Confira se o conjunto está vazio;
 */
public class ExercicioPropostoSet {
    public static void main(String[] args) {
        System.out.println("Crie uma conjunto contendo as cores do arco-iris: ");
        Set<String> coresArcoIris = new HashSet<>();
        coresArcoIris.add("violeta");
        coresArcoIris.add("anil");
        coresArcoIris.add("azul");
        coresArcoIris.add("verde");
        coresArcoIris.add("amarelo");
        coresArcoIris.add("laranja");
        coresArcoIris.add("vermelho");
        System.out.println(coresArcoIris);

        System.out.println("Exiba todas as cores o arco-iris uma abaixo da outra: ");
        for (String cor : coresArcoIris) {
            System.out.println(cor);
        }

        System.out.println("A quantidade de cores que o arco-iris tem: " + coresArcoIris.size());

        System.out.println("Exiba as cores em ordem alfabetica: ");
        Set<String> coresArcoIris2 = new TreeSet<>(coresArcoIris);
        System.out.println(coresArcoIris2);

        System.out.println("Exiba as cores na ordem inversa da que foi informada ");
        Set<String> coresArcoIris3 = new LinkedHashSet<>(
                Arrays.asList("violeta", "anil", "azul", "verde", "amarelo", "laranja", "vermelho"));
        System.out.println(coresArcoIris3);
        List<String> coresArcoIrisList = new ArrayList<>(coresArcoIris3);
        Collections.reverse(coresArcoIrisList);
        System.out.println(coresArcoIrisList);

        System.out.println("Exiba todas as cores que comecam com a letra ”v”: ");
        for (String cor: coresArcoIris) {
            if(cor.startsWith("v")) System.out.println(cor);
        }

        System.out.println("Remova todas as cores que nao comecam com a letra “v”: ");
        Iterator<String> iterator2 = coresArcoIris.iterator();
        while (iterator2.hasNext()) {
            if (!iterator2.next().startsWith("v")) iterator2.remove();
        }
        System.out.println(coresArcoIris);

        System.out.println("Limpe o conjunto: ");
        coresArcoIris.clear();

        System.out.println("Confira se o conjunto esta vazio: " + coresArcoIris.isEmpty());
    }

###  C:\Users\Irene\.jdks\openjdk-18.0.1.1\bin\java.exe "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.1.1\lib\idea_rt.jar=57016:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.1.1\bin" -Dfile.encoding=UTF-8 -classpath "C:\Users\Irene\Documents\ExercicioProposto02.java Set\ExercicioProposto2.java.Set\out\production\ExercicioProposto2.java.Set" fe.com.ExercicioPropostoSet
Crie uma conjunto contendo as cores do arco-iris: 
[vermelho, amarelo, violeta, verde, laranja, anil, azul]
Exiba todas as cores o arco-iris uma abaixo da outra: 
vermelho
amarelo
violeta
verde
laranja
anil
azul
A quantidade de cores que o arco-iris tem: 7
Exiba as cores em ordem alfabetica: 
[amarelo, anil, azul, laranja, verde, vermelho, violeta]
Exiba as cores na ordem inversa da que foi informada 
[violeta, anil, azul, verde, amarelo, laranja, vermelho]
[vermelho, laranja, amarelo, verde, azul, anil, violeta]
Exiba todas as cores que comecam com a letra �v�: 
vermelho
violeta
verde
Remova todas as cores que nao comecam com a letra �v�: 
[vermelho, violeta, verde]
Limpe o conjunto: 
Confira se o conjunto esta vazio: true

Process finished with exit code 0
