# CNPJ Grátis
<!-- [![Travis](https://travis-ci.org/brk-labs/cnpj-gratis.svg?branch=2.0)](https://travis-ci.org/brk-labs/cnpj-gratis) -->
[![Latest Stable Version](https://poser.pugx.org/brk-labs/cnpj-gratis/v/stable.svg)](https://packagist.org/packages/brk-labs/cnpj-gratis) 
[![Total Downloads](https://poser.pugx.org/brk-labs/cnpj-gratis/downloads.svg)](https://packagist.org/packages/brk-labs/cnpj-gratis) 
[![Latest Unstable Version](https://poser.pugx.org/brk-labs/cnpj-gratis/v/unstable.svg)](https://packagist.org/packages/brk-labs/cnpj-gratis)
[![MIT license](https://poser.pugx.org/brk-labs/nfephp-serialize/license.svg)](http://opensource.org/licenses/MIT)

Com esse pacote você poderá realizar consultas de CNPJ no site da Receita Federal do Brasil gratuitamente.

Atenção: Esse pacote não possui leitor de captcha, mas captura o mesmo para ser digitado pelo usuário

### Changelog

*1.0.5 correcao do http

### Como utilizar

Adicione a library

```sh
$ composer require brk-labs/cnpj-gratis
```

Adicione o autoload.php do composer no seu arquivo PHP.

```php
require_once 'vendor/autoload.php';  
```

Primeiro chame o método `getParams()` para retornar os dados necessários para enviar no método `consulta()` 

```php
$params = brk-labs\CnpjGratis\CnpjGratis::getParams();
```

Agora basta chamar o método `consulta()`

```php
$dadosEmpresa = brk-labs\CnpjGratis\CnpjGratis::consulta(
    '45.543.915/0001-81',
    'INFORME_AS_LETRAS_DO_CAPTCHA',
    $params['cookie']
);
```
<!-- 
### Gostou? Conheça também

* [CpfGratis](https://github.com/brk-labs/cpf-gratis)
* [CepGratis](https://github.com/brk-labs/cep-gratis)
* [CidadesGratis](https://github.com/brk-labs/cidades-gratis)
* [NFePHPSerialize](https://github.com/brk-labs/nfephp-serialize) -->

### License

The MIT License (MIT)
