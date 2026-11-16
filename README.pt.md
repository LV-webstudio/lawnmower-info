# Shania Lawnmower — auditoria de sites: SEO, segurança e acessibilidade

> Uma aplicação de ambiente de trabalho para Windows de auditoria web inteligente: escolha um site, um modo e leia um relatório em linguagem clara.

Por [Shania Webstudio](https://shaniawebstudio.com), Granada (Espanha).

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · **Português**

![Shania Lawnmower](assets/banner.jpg)

*Banner de marca da Shania Lawnmower (ilustração).*

## O que é

A Shania Lawnmower é a face de ambiente de trabalho do motor de análise web da Shania. Escolhe um endereço web, um modo e um módulo, e a aplicação executa a análise e abre um relatório HTML que explica cada constatação em linguagem clara: o que acontece, porque importa, como corrigir e como verificar a correção. Propõe correções, mas nunca altera o seu site.

## Para quem

- Pequenas empresas e agências que querem saber o que falha no seu site (cabeçalhos de segurança, privacidade, velocidade, acessibilidade, SEO).
- Estúdios que auditam os seus próprios sites ou os de clientes que deram autorização.

## O que faz

- Modos de análise rápida e completa; a completa acrescenta o Lighthouse (desempenho, SEO) e verificações de acessibilidade e requer o Google Chrome instalado.
- Modo passivo (o que qualquer visitante vê) e modo autorizado para domínios próprios ou com permissão, controlado por uma lista de permissões.
- Sinais públicos sobre privacidade e cookies, páginas legais, rastreadores, fornecedores de pagamento e menções ao VeriFactu. São indícios, não certificações.
- Relatório de constatações e plano de correção que apenas recomenda; não altera ficheiros nem o site remoto.
- Monitorização local: repete a análise a cada 24 horas enquanto a aplicação está aberta e compara as constatações com a referência guardada.
- Um perfil ativo limitado que fica bloqueado a menos que existam contrato assinado, âmbito definido e revisão profissional independente documentados. Não é um teste de intrusão e não faz exploração, força bruta nem varrimento de portas.

## Estado

**Em desenvolvimento (MVP)**

A aplicação compila-se como instalador de Windows, mas a instalação num Windows limpo e um piloto com sites reais ainda estão pendentes. Ainda não é oferecida como serviço a clientes. Requer Node.js 20 ou superior no PC.

## O motor: Analitics

A Shania Lawnmower funciona sobre o Analitics, o motor de análise de linha de comandos da Shania Webstudio, que também pode ser usado em separado a partir de um terminal (Node.js 20 ou superior).

- Áreas que cobre: segurança, privacidade, desempenho, acessibilidade, qualidade e SEO. Cada constatação diz o que acontece, porque importa, como corrigir, como verificar a correção e com que confiança e evidência a ferramenta o afirma.
- Com a opção completa e o Chrome instalado: Lighthouse (mediana de três passagens por dispositivo) e verificações de acessibilidade com axe (WCAG A/AA).
- Coletores de SEO e de preparação para IA (HTML, rastreio, metadados) e uma pontuação global com limites explícitos para constatações graves.
- Três modos: passivo (por omissão), autorizado (apenas domínios da lista de permissões) e um perfil ativo limitado que fica bloqueado sem contrato, âmbito e revisão profissional independente documentados.
- Os testes automáticos cobrem as opções, as proteções de autorização, os erros dos coletores e os relatórios.
- Limites: é uma ferramenta local, não um serviço de auditoria implementável, e não certifica nada; as verificações legais, fiscais e de pagamentos apenas mostram sinais públicos. As transferências de dados para o W3C, a Cloudflare e um repositório público são descritas mais abaixo.

## Dados que convém conhecer

O validador de HTML recebe o HTML da página (W3C), as verificações de DNS usam o DNS sobre HTTPS da Cloudflare e a lista de vulnerabilidades de bibliotecas é descarregada de um repositório público. Não a use em páginas confidenciais sem rever estas transferências.

## Sobre este repositório

Este repositório contém apenas informação: o código é privado.

## Contacto

- E-mail: hola@shaniawebstudio.com
- Site: https://shaniawebstudio.com

---
*Um produto da Shania Webstudio.* · Copyright (c) 2026 Shania Webstudio.
