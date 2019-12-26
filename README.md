# CNPJ Grátis
[![Travis](https://travis-ci.org/gleisonnanet/cnpj-gratis.svg?branch=2.0)](https://travis-ci.org/gleisonnanet/cnpj-gratis)
[![Latest Stable Version](https://poser.pugx.org/gleisonnanet/cnpj-gratis/v/stable.svg)](https://packagist.org/packages/gleisonnanet/cnpj-gratis) 
[![Total Downloads](https://poser.pugx.org/gleisonnanet/cnpj-gratis/downloads.svg)](https://packagist.org/packages/gleisonnanet/cnpj-gratis) 
[![Latest Unstable Version](https://poser.pugx.org/gleisonnanet/cnpj-gratis/v/unstable.svg)](https://packagist.org/packages/gleisonnanet/cnpj-gratis)
[![MIT license](https://poser.pugx.org/gleisonnanet/nfephp-serialize/license.svg)](http://opensource.org/licenses/MIT)

Com esse pacote você poderá realizar consultas de CNPJ no site da Receita Federal do Brasil gratuitamente.

Atenção: Esse pacote não possui leitor de captcha, mas captura o mesmo para ser digitado pelo usuário

### Changelog

* 2.1.1 - Bugfix: Atualização site receita. Obrigado @fernandobatels
* 2.1.0 - Removendo dependências extras e versão mínima PHP 5.5
* 2.0.8 - Bugfix: Campo telefone quando não informado. Obrigado @mprandot
* 2.0.7 - Bugfix: Atualização site receita. Obrigado @Marciobds

### Como utilizar

Adicione a library

```sh
$ composer require gleisonnanet/cnpj-gratis
```

Adicione o autoload.php do composer no seu arquivo PHP.

```php
require_once 'vendor/autoload.php';  
```

Primeiro chame o método `getParams()` para retornar os dados necessários para enviar no método `consulta()` 

```php
$params = gleisonnanet\CnpjGratis\CnpjGratis::getParams();
```

Agora basta chamar o método `consulta()`

```php
$dadosEmpresa = gleisonnanet\CnpjGratis\CnpjGratis::consulta(
    '45.543.915/0001-81',
    'INFORME_AS_LETRAS_DO_CAPTCHA',
    $params['cookie']
);
```

### Gostou? Conheça também

* [CpfGratis](https://github.com/gleisonnanet/cpf-gratis)
* [CepGratis](https://github.com/gleisonnanet/cep-gratis)
* [CidadesGratis](https://github.com/gleisonnanet/cidades-gratis)
* [NFePHPSerialize](https://github.com/gleisonnanet/nfephp-serialize)

### License

The MIT License (MIT)
