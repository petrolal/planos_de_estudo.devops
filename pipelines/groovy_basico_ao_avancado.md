# 📘 Plano de Estudos: Groovy (para Devs/DevOps, Jenkins e Gradle)

## 🎯 Objetivo
Aprender Groovy do zero até tópicos avançados (DSLs, metaprogramação, AST transforms), com foco em automação, **Jenkins Pipelines**, **Gradle** e scripts de produtividade em ambiente Java.

---

## 📍 Pré-requisitos
- Lógica de programação e noções de **Java** (opcional, mas ajuda).
- Ambiente Java (JDK 17+), **SDKMAN!** para instalar Groovy/Gradle.
- Editor (VS Code/IntelliJ) e terminal Linux/macOS/WSL.

---

## 🔧 Setup Rápido
- SDKMAN!: `curl -s "https://get.sdkman.io" | bash`
- Instalar Groovy: `sdk install groovy`
- REPL/Console: `groovyConsole` ou `groovysh`

---

## 🟢 Básico

### 1) Fundamentos de Groovy
- Tipagem dinâmica/estática (def, var, `@CompileStatic`).
- Sintaxe essencial: variáveis, `if/else`, loops, `switch`, strings (GStrings).
- Funções e **closures** (parâmetros implícitos `it`, currying).
- **Coleções**: List, Map, Range; operadores poderosos (`*.`, `collect`, `find`, `findAll`, `grep`).
- **GDK** (extensões da API Java): manipulação de arquivos, URLs, datas.
  
**Exemplo:**
```groovy
def nums = [1,2,3,4,5]
println nums.findAll { it % 2 == 0 }.collect { it * 10 }   // [20, 40]
new File('hosts.txt').eachLine { println it }
```

### 2) OO no Groovy
- Classes, propriedades, construtores, `@ToString`, `@EqualsAndHashCode`.
- Operadores sobrecarregados (ex.: `<<`, `+` em coleções).
- Pacotes e interoperabilidade com Java.

---

## 🟡 Intermediário

### 3) Builders & DSLs
- **MarkupBuilder** (XML/HTML), **JsonBuilder**.
- **ConfigSlurper** (ler `.groovy` de config).
- Criando DSLs simples (ex.: tarefas de deploy, pipelines locais).

```groovy
def html = new groovy.xml.MarkupBuilder()
html.html {
  body { h1 "Hello, Groovy!" }
}
```

### 4) IO, JSON/YAML & HTTP
- Ler/gravar arquivos, `withWriter`, `text`, `newReader`.
- JSON (JsonSlurper/JsonOutput), YAML (via lib SnakeYAML).
- HTTP rápido com `@Grab('org.codehaus.groovy:groovy-json')` + `URL#text` ou libs (HTTPBuilder/OkHttp).

### 5) Testes com **Spock**
- Especificações BDD: `given/when/then`.
- Mocks/Stubs, data tables.
- Testar scripts e pipelines (lib Jenkins Pipeline Unit).

### 6) Convergência com o ecossistema
- **Gradle (Groovy DSL)**: tasks, plugins, `build.gradle`.
- **Jenkins Pipeline (Scripted/Declarative)**: stages, steps, shared libraries.
- Segurança: sandbox de Groovy em Jenkins.

---

## 🔴 Avançado

### 7) Metaprogramação
- Categories, `ExpandoMetaClass`, métodos dinâmicos.
- Operator overloading, interceptors, `methodMissing`/`propertyMissing`.
- Cuidados de manutenção e performance.

### 8) **AST Transformations**
- Anotações padrão: `@Immutable`, `@Canonical`, `@Singleton`, `@Builder`, `@TupleConstructor`, `@Memoized`.
- `@CompileStatic` e `@TypeChecked` para performance/segurança.
- Criando transforms (conceito) e onde usar (geração de boilerplate).

### 9) Concorrência
- **GPars** (actors, dataflow, parallel collections).
- Paralelizar pipelines/transformações de dados.
- Alternativas modernas (Executors/Virtual Threads no Java) e interoperabilidade.

### 10) Performance & Boas Práticas
- Quando usar Groovy dinâmico vs estático.
- Perfilamento (JFR/VisualVM), hotspots comuns.
- Estrutura de projeto, empacotamento (fat jars), logging, versionamento.

---

## 🛠️ Groovy para **Jenkins**
- **Declarative vs Scripted Pipeline**: quando escolher cada um.
- Steps essenciais: `checkout`, `sh`, `withCredentials`, `archiveArtifacts`, `stash/unstash`, `parallel`.
- **Shared Libraries** (vars/, src/): reutilização, testes com **Jenkins Pipeline Unit**.
- Patterns úteis: pipelines para microserviços, matrix builds, promotion, multibranch.
- Segurança (sandbox), permissões, `@NonCPS`.

**Exemplo (Declarative)**
```groovy
pipeline {
  agent any
  stages {
    stage('Build') { steps { sh 'mvn -B -DskipTests package' } }
    stage('Test')  { steps { sh 'mvn test' } }
    stage('Docker'){ steps { sh 'docker build -t org/app:${BUILD_NUMBER} .' } }
  }
}
```

---

## 🔩 Groovy para **Gradle (Groovy DSL)**
- Estrutura `build.gradle`, `settings.gradle`.
- Tasks (`task myTask { doLast { ... } }`), dependências, repositórios.
- Plugins (Java, Spring Boot, Docker, Sonar, Jacoco).
- Multi-módulos, versões e catálogos de libs.
- Migração para Kotlin DSL (comparativo rápido).

**Exemplo**
```groovy
plugins { id 'java' }
repositories { mavenCentral() }
dependencies { testImplementation 'org.spockframework:spock-core:2.3-groovy-4.0' }
test { useJUnitPlatform() }
```

---

## 🧪 Projeto Prático (capstone)
1. **CLI em Groovy**: script que lê YAML/JSON, executa etapas (build/test/package) e publica artefatos.
2. **Jenkins Pipeline real** para um serviço Java 21:
   - stages: build, test, quality, docker build/push, deploy (Swarm/K8s).
   - uso de `withCredentials`, `stash`, `parallel` e **Shared Library** para steps comuns.
3. **Gradle**: `build.gradle` com Spock, Jacoco, Sonar e task custom para versionamento semântico.

---

## 📅 Cronograma Sugerido (4 semanas)
- **Semana 1**: Fundamentos + OO + GDK + coleções/closures.
- **Semana 2**: Builders/DSLs, IO/HTTP/JSON/YAML, Spock.
- **Semana 3**: Gradle (Groovy DSL) + Jenkins Pipeline + Shared Libs.
- **Semana 4**: Metaprogramação, AST, concorrência, performance + Projeto final.

---

## 📚 Referências Curadas
- *Groovy Language Documentation* (groovy-lang.org)
- *Spock Framework Reference*
- *Gradle User Guide (Groovy DSL)*
- *Jenkins Pipeline Syntax* e *Shared Libraries*
- **Livro**: *Making Java Groovy* (Kenneth Kousen) – ótimo para interoperar com Java

---

## ✅ Checklist de Domínio
- [ ] Sintaxe, GStrings, closures, coleções.
- [ ] GDK e IO; JSON/YAML/HTTP.
- [ ] Spock e testes.
- [ ] Gradle (Groovy DSL).
- [ ] Jenkins Pipeline + Shared Libraries (com testes).
- [ ] Metaprogramação e AST transforms.
- [ ] Performance e melhores práticas.
