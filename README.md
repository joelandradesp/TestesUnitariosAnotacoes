# Testes Unitários - Anotacoes

Anotações de Testes Unitários - JUnit, AssertJ, Mockito, exemplos em Java.

JUnit é uma Framework de testes unitários que fornece para nós um ambiente de execução e de escrita de testes unitários.

Mockito é uma biblioteca de testes unitários que vai nos oferecer uma série de ferramentas auxiliares para que agente escreve Mocks dentro dos nossos testes unitários. 

Quando agente esta falando do Spring, então quanod agente tá falando de testes unitários no Framework Spring, tem outra bibliotecaque vai entrar em jogo, Spring Boot Starter Test, e muito provavelmente essa biblioteca já vai vir instalada no seu projeto se você tiver inicializado ele usando o Spring Initializer. Então por padrão o String Initializer já costuma adicionar como dependência essa biblioteca aqui Spring Boot Starter Test e a gente não precisa instalar nenhuma biblioteca a mais por enquanto para fazer a escrita dos nossos testes.

Spring Boot Starter Test é um pack de bibliotecas de teste unitário e dentro delta tem o JUnit, tem o moquito, tem o AssertJ.

Documentação Spring Boot Starter Test  [Spring Boot Starter Test](https://docs.spring.io/spring-boot/docs/1.5.7.RELEASE/reference/html/boot-features-testing.html).

## Dependências do escopo de teste

Se você usar o spring-boot-starter-test'Starter' (no arquivo test scope), você encontrará as seguintes bibliotecas fornecidas:

JUnit — O padrão de fato para testes unitários de aplicativos Java.
Spring Test e Spring Boot Test — Utilitários e suporte a testes de integração para aplicativos Spring Boot.
AssertJ — Uma biblioteca de asserções fluente.
Hamcrest — Uma biblioteca de objetos correspondentes (também conhecidos como restrições ou predicados).
Mockito — Uma estrutura de simulação Java.
JSONassert — Uma biblioteca de asserções para JSON.
JsonPath — XPath para JSON.

## Testar anotações de configuração automática

Aqui está uma tabela das diversas @…Testanotações que podem ser usadas para testar fatias do seu aplicativo e a configuração automática que elas importam por padrão:


Anotações de configuração Automática [Anotações de configuração Automática](https://docs.spring.io/spring-boot/docs/1.5.7.RELEASE/reference/html/test-auto-configuration.html).

## AssertJ

Vamos supor que temos um cenário de teste em que queremos verificar se a variável a é igual à variável b.

Utilizando apenas JUnit ficaríamos com o seguinte código:

```

assertEquals(b, a);

```

Escrevemos primeiro o valor esperado e, só depois, o valor real.

E teríamos a seguinte importação: 

```

** import static ** org.junit.Assert.assertEquals;

```

### Hamcrest

```

assertThat(a, equalTo(b));


```

E os **import**s:

```

import static org.hamcrest.MatcherAssert.assertThat;
import static org.hamcrest.Matchers.equalTo;

```

É possível observar que agora escrevemos na ordem que esperamos, ou seja, primeiro o valor real, depois o esperado. Um outro ponto é que aumentamos o número de imports para dois, mas isso é totalmente aceitável.


### AssertJ

```

assertThat(a).isEqualTo(b);

```

E teríamos o seguinte **import**:

```

import static org.assertj.core.api.Assertions.assertThat;


```

Convertendo suas asserções JUnit 3 e 4 para AssertJ [Anotações de configuração Automática](https://joel-costigliola.github.io/assertj/assertj-core-converting-junit-assertions-to-assertj.html).

