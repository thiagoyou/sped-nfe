## Introdução

Esse documento tem o objetivo de ser um passo a passo inicial para que você possa emitir as suas notas com SPED-NFE. Mas antes de começar vou dar uma breve explicação do que são as NF-e e como funciona o seu processo de emissão.

## O que são Nf-e/Nfc-e?
Uma nota fiscal eletrônica nada mais é do que um arquivo XML que contém informações dos produtos vendidos ou serviços prestados por você com todas as informações tributárias necessárias exigidas pela receita. Esse arquivo é assinado com um certificado digital e enviado para a receita.

Segue um exemplo do XML gerado pelo framework ainda sem a assinatura do certificado e o protocolo.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<NFe xmlns="http://www.portalfiscal.inf.br/nfe">
    <infNFe Id="NFe35180278767865000156550010000000021800700088" versao="3.10">
        <ide>
            <cUF>35</cUF>
            <cNF>80070008</cNF>
            <natOp>VENDA</natOp>
            <indPag>0</indPag>
            <mod>55</mod>
            <serie>1</serie>
            <nNF>2</nNF>
            <dhEmi>2018-02-06T20:48:00-02:00</dhEmi>
            <dhSaiEnt>2018-02-06T20:48:00-02:00</dhSaiEnt>
            <tpNF>1</tpNF>
            <idDest>1</idDest>
            <cMunFG>3518800</cMunFG>
            <tpImp>1</tpImp>
            <tpEmis>1</tpEmis>
            <cDV>8</cDV>
            <tpAmb>2</tpAmb>
            <finNFe>1</finNFe>
            <indFinal>0</indFinal>
            <indPres>0</indPres>
            <procEmi>3.10.31</procEmi>
            <verProc>1</verProc>
        </ide>
    <emit>
        <CNPJ>78767865000156</CNPJ>
        <xNome>Empresa teste</xNome>
        <enderEmit>
            <xLgr>Rua Teste</xLgr>
            <nro>203</nro>
            <xBairro>Centro</xBairro>
            <cMun>4317608</cMun>
            <xMun>Porto Alegre</xMun>
            <UF>RS</UF>
            <CEP>955500000</CEP>
            <cPais>1058</cPais>
            <xPais>BRASIL</xPais>
        </enderEmit>
        <IE>6564344535</IE>
        <CRT>3</CRT>
    </emit>
    <dest>
        <CNPJ>78767865000156</CNPJ>
        <xNome>NF-E EMITIDA EM AMBIENTE DE HOMOLOGACAO - SEM VALOR FISCAL</xNome>
        <enderDest>
            <xLgr>Rua Teste</xLgr>
            <nro>203</nro>
            <xBairro>Centro</xBairro>
            <cMun>4317608</cMun>
            <xMun>Porto Alegre</xMun>
            <UF>RS</UF>
            <CEP>955500-000</CEP>
            <cPais>1058</cPais>
            <xPais>BRASIL</xPais>
        </enderDest>
        <indIEDest>1</indIEDest>
        <IE>6564344535</IE>
    </dest>
    <det nItem="1">
        <prod>
            <cProd>0001</cProd>
            <cEAN/>
            <xProd>Produto teste</xProd>
            <NCM>66554433</NCM>
            <CFOP>5102</CFOP>
            <uCom>PÇ</uCom>
            <qCom>1.0000</qCom>
            <vUnCom>10.99</vUnCom>
            <vProd>10.99</vProd>
            <cEANTrib/>
            <uTrib>PÇ</uTrib>
            <qTrib>1.0000</qTrib>
            <vUnTrib>10.99</vUnTrib>
            <indTot>1</indTot>
        </prod>
            <imposto>
            <vTotTrib>10.99</vTotTrib>
            <ICMS>
                <ICMS00>
                    <orig>0</orig>
                    <CST>00</CST>
                    <modBC>0</modBC>
                    <vBC>0.2</vBC>
                    <pICMS>18.0000</pICMS>
                    <vICMS>0.04</vICMS>
                </ICMS00>
            </ICMS>
            <IPI>
                <cEnq>999</cEnq>
                <IPITrib>
                <CST>50</CST>
                <vIPI>0</vIPI>
                </IPITrib>
            </IPI>
            <PIS>
                <PISNT>
                <CST>07</CST>
                </PISNT>
            </PIS>
            <COFINSST>
                <vBC>0</vBC>
                <pCOFINS>0</pCOFINS>
                <qBCProd/>
                <vAliqProd/>
                <vCOFINS>0</vCOFINS>
            </COFINSST>
        </imposto>
    </det>
    <total>
        <ICMSTot>
            <vBC>0.20</vBC>
            <vICMS>0.04</vICMS>
            <vICMSDeson>0.00</vICMSDeson>
            <vBCST>0.00</vBCST>
            <vST>0.00</vST>
            <vProd>10.99</vProd>
            <vFrete>0.00</vFrete>
            <vSeg>0.00</vSeg>
            <vDesc>0.00</vDesc>
            <vII>0.00</vII>
            <vIPI>0.00</vIPI>
            <vPIS>0.00</vPIS>
            <vCOFINS>0.00</vCOFINS>
            <vOutro>0.00</vOutro>
            <vNF>11.03</vNF>
            <vTotTrib>10.99</vTotTrib>
        </ICMSTot>
    </total>
    <transp>
        <modFrete>1</modFrete>
        <vol>
            <qVol>2</qVol>
            <esp>caixa</esp>
            <marca>OLX</marca>
            <nVol>11111</nVol>
            <pesoL>10</pesoL>
            <pesoB>11</pesoB>
        </vol>
    </transp>
    <cobr>
        <fat>
            <nFat>100</nFat>
            <vOrig>100</vOrig>
            <vLiq>100</vLiq>
        </fat>
        <dup>
            <nDup>100</nDup>
            <dVenc>2017-08-22</dVenc>
            <vDup>11.03</vDup>
            </dup>
        </cobr>
</infNFe>
</NFe>
```
## Como vamos fazer isso?
Nesse passo a passo vamos passar por todas as etapas desse processo. Primeiro: a montagem do XML, como no exemplo acima; Segundo: a sua assinatura usando um certificado digital; Terceiro: o envio para a receita. Quarto: vamos consultar o nosso envio para ver se tudo ocorreu como nós esperamos; Por fim vamos pegar o protocolo que recebemos da consulta para armazenar no XML.

## Requisitos
Antes de falarmos de código, você precisa ter em mãos o seu certificado digital do tipo A1. Ele é um tipo de certificado que pode ser instalado no computador, normalmente um arquivo com a extensão *.pfx* que pode ser usado sem a necessidade de um token externo. Caso você não tenha o certificado você pode ir ao cartório da sua cidade que lá eles vão te auxiliar no processo para conseguir o seu.

Para a instalação do framework você precisa verificar se as seguintes extensões do PHP estão ativas no seu PHP:
* PHP 5.6 ou PHP 7.x (recomendável PHP 7.x)
* ext-curl
* ext-dom
* ext-json
* ext-gd
* ext-mbstring
* ext-mcrypt
* ext-openssl
* ext-soap
* ext-xml
* ext-zip

Com as extensões devidamente instaladas, basta criar um pasta para o seu projeto e dentro dela rodar o seguinte comando com o composer
```bash
composer require nfephp-org/sped-nfe
```

Rodando esse comando vamos instalar a última versão do framework hoje, que é a versão 5.0 capaz de emitir Nf-e e Nfc-e na versão 3.10 e 4.0.

## Montar XML
Agora com framework devidamente instalando podemos partir para a montagem do XML. Vamos criar um arquivo *index.php* dentro do seu projeto e nele colocar o código abaixo.
```php
<?php
require_once "vendor/autoload.php";

$nfe = new NFePHP\NFe\Make();

$std = new \stdClass();
$std->versao = '3.10';
$nfe->taginfNFe($std);

$std = new \stdClass();
$std->cUF = 35;
$std->cNF = '80070008';
$std->natOp = 'VENDA';
$std->indPag = 0;
$std->mod = 55;
$std->serie = 1;
$std->nNF = 2;
$std->dhEmi = '2018-02-06T20:48:00-02:00';
$std->dhSaiEnt = '2018-02-06T20:48:00-02:00';
$std->tpNF = 1;
$std->idDest = 1;
$std->cMunFG = 3518800;
$std->tpImp = 1;
$std->tpEmis = 1;
$std->cDV = 2;
$std->tpAmb = 2; // Se deixar o tpAmb como 2 você emitirá a nota em ambiente de homologação(teste) e as notas fiscais aqui não tem valor fiscal
$std->finNFe = 1;
$std->indFinal = 0;
$std->indPres = 0;
$std->procEmi = '3.10.31';
$std->verProc = 1;
$nfe->tagide($std);

$std = new \stdClass();
$std->xNome = 'Empresa teste';
$std->IE = '6564344535';
$std->CRT = 3;
$std->CNPJ = '78767865000156';
$nfe->tagemit($std);

$std = new \stdClass();
$std->xLgr = "Rua Teste";
$std->nro = '203';
$std->xBairro = 'Centro';
$std->cMun = '4317608';
$std->xMun = 'Porto Alegre';
$std->UF = 'RS';
$std->CEP = '955500-000';
$std->cPais = '1058';
$std->xPais = 'BRASIL';
$nfe->tagenderEmit($std);

$std = new \stdClass();
$std->xNome = 'Empresa destinatário teste';
$std->indIEDest = 1;
$std->IE = '6564344535';
$std->CNPJ = '78767865000156';
$nfe->tagdest($std);

$std = new \stdClass();
$std->xLgr = "Rua Teste";
$std->nro = '203';
$std->xBairro = 'Centro';
$std->cMun = '4317608';
$std->xMun = 'Porto Alegre';
$std->UF = 'RS';
$std->CEP = '955500-000';
$std->cPais = '1058';
$std->xPais = 'BRASIL';
$nfe->tagenderDest($std);

$std = new \stdClass();
$std->item = 1;
$std->cProd = '0001';
$std->xProd = "Produto teste";
$std->NCM = '66554433';
$std->CFOP = '5102';
$std->uCom = 'PÇ';
$std->qCom = '1.0000';
$std->vUnCom = '10.99';
$std->vProd = '10.99';
$std->uTrib = 'PÇ';
$std->qTrib = '1.0000';
$std->vUnTrib = '10.99';
$std->indTot = 1;
$nfe->tagprod($std);

$std = new \stdClass();
$std->item = 1;
$std->vTotTrib = 10.99;
$nfe->tagimposto($std);

$std = new \stdClass();
$std->item = 1;
$std->orig = 0;
$std->CST = '00';
$std->modBC = 0;
$std->vBC = 0.20;
$std->pICMS = '18.0000';
$std->vICMS ='0.04';
$nfe->tagICMS($std);

$std = new \stdClass();
$std->item = 1;
$std->cEnq = '999';
$std->CST = '50';
$std->vIPI = 0;
$std->vBC = 0;
$std->pIPI = 0;
$nfe->tagIPI($std);

$std = new \stdClass();
$std->item = 1;
$std->CST = '07';
$std->vBC = 0;
$std->pPIS = 0;
$std->vPIS = 0;
$nfe->tagPIS($std);

$std = new \stdClass();
$std->item = 1;
$std->vCOFINS = 0;
$std->vBC = 0;
$std->pCOFINS = 0;
$nfe->tagCOFINSST($std);

$std = new \stdClass();
$std->vBC = 0.20;
$std->vICMS = 0.04;
$std->vICMSDeson = 0.00;
$std->vBCST = 0.00;
$std->vST = 0.00;
$std->vProd = 10.99;
$std->vFrete = 0.00;
$std->vSeg = 0.00;
$std->vDesc = 0.00;
$std->vII = 0.00;
$std->vIPI = 0.00;
$std->vPIS = 0.00;
$std->vCOFINS = 0.00;
$std->vOutro = 0.00;
$std->vNF = 11.03;
$std->vTotTrib = 0.00;
$nfe->tagICMSTot($std);

$std = new \stdClass();
$std->modFrete = 1;
$nfe->tagtransp($std);

$std = new \stdClass();
$std->item = 1;
$std->qVol = 2;
$std->esp = 'caixa';
$std->marca = 'OLX';
$std->nVol = '11111';
$std->pesoL = 10.00;
$std->pesoB = 11.00;
$nfe->tagvol($std);

$std = new \stdClass();
$std->nFat = '100';
$std->vOrig = 100;
$std->vLiq = 100;
$nfe->tagfat($std);

$std = new \stdClass();
$std->nDup = '100';
$std->dVenc = '2017-08-22';
$std->vDup = 11.03;
$nfe->tagdup($std);

$xml = $nfe->getXML(); // O conteúdo do XML fica armazenado na variável $xml
```
Esse exemplo são só alguns campos que podem ser preenchidos para emitir uma Nf-e, mas existem muito mais. Abordar todos os campos seria bastante complicado, para cada situação a nota deve ser preenchida com um campo ou outro. Se você não tem um bom domínio sobre contabilidade o meu concelho é sempre perguntar para alguem que saiba como deve ser preenchida a nota na situação em questão.

> Para saber todos os campos suportados pelo framework acesse o link da documentação https://github.com/nfephp-org/sped-nfe/blob/master/docs/Make.md

## Assinar XML
Antes de assinarmos o XML precisamos criar um variável em *JSON* com os dados que o framework vai precisar para os próximos passos.
```php
$config = [
   "atualizacao" => "2018-02-06 06:01:21",
   "tpAmb" => 2, // Se deixar o tpAmb como 2 você emitirá a nota em ambiente de homologação(teste) e as notas fiscais aqui não tem valor fiscal
   "razaosocial" => "Empresa teste",
   "siglaUF" => "RS",
   "cnpj" => "78767865000156",
   "schemes" => "PL_008i2",
   "versao" => "3.10",
   "tokenIBPT" => "AAAAAAA"
];
$configJson = json_encode($config);
```
E vamos precisar do certificado digital mencionado anteriormente.
```php
$certificadoDigital = file_get_contents('certificado.pfx');
```

Agora que temos o nosso *$xml* gerado do passo anterior, a *$configJson* e o nosso $certificadoDigital* já estamos pronto para assiná-lo.

Cole os seguinte código no seu arquivo *index.php*. Lembrando de substituir a *'senha do certificado'* pela senha correta.
```php
$tools = new NFePHP\NFe\Tools($configJson, NFePHP\Common\Certificate::readPfx($certificadoDigital, 'senha do certificado'));
$xmlAssinado = $tools->signNFe($xml); // O conteúdo do XML assinado fica armazenado na variável $xmlAssinado
```
> Mais uma vez caso precise de mais detalhes sobre como funciona o método de assinatura você pode consultar a documentação acessando o link https://github.com/nfephp-org/sped-nfe/blob/master/docs/metodos/SignNFe.md

## Enviar Lote
Para o envio do lote vamos precisar da *$configJson*, *$certificadoDigital* e do nosso XML assinado que está na variável *$xmlAssinado*. Esse método recebe um array com os XMLs nos permitindo enviar mais de um XML por vez, mas nesse caso vamos enviar somente um.
```php
$idLote = str_pad(100, 15, '0', STR_PAD_LEFT); // Identificador do lote
$resp = $this->tools->sefazEnviaLote([$xmlAssinado], $idLote);

$st = new NFePHP\NFe\Common\Standardize();
$std = $st->toStd($resp);
if ($std->cStat != 103) {
   //erro registrar e voltar
   exit("[$std->cStat] $std->xMotivo");
}
$recibo = $std->infRec->nRec; // Vamos usar a variável $recibo para consultar o status da nota
```
Usamos a classe *Standardize* para converter o XML retornado pela receita para o formato *StdClass* assim caso o atributo *$std->cStat* retorne algo diferente de 103 sabemos algo deu errado no envio do lote para a receita.
> Caso você precise de mais detalhes acesse o link da documentação https://github.com/nfephp-org/sped-nfe/blob/master/docs/metodos/EnviaLote.md

## Consultar Recibo
Com o recibo retornado pelo método *sefazEnviaLote* vamos ver se nota foi autorizada ou rejeitada pela receita. Vamos precisar da *$configJson*, *$certificadoDigital* e do número de recibo que temos na variável *$recibo*.
```php
$tools = new NFePHP\NFe\Tools($configJson, NFePHP\Common\Certificate::readPfx($certificadoDigital, 'senha do certificado'));
$protocolo = $this->tools->sefazConsultaRecibo($recibo);
```
> Para detalhes acesse o link da documentação https://github.com/nfephp-org/sped-nfe/blob/master/docs/metodos/ConsultaRecibo.md

Agora com variável *$protocolo* temos o resultado se a nossa nota foi autorizada ou rejeitada.

## Finalizando o processo
Agora que enviamos a nota, consultamos o seu status, vamos trabalhar a com a situação a onde tudo deu certo e a nota foi autorizada. Precisamos guardar esse protocolo dentro do nosso XML, vamos pegar a nossa *$xmlAssinado* e a *$protocolo* e usar o código abaixo.
```php
$protocol = new NFePHP\NFe\Factories\Protocol();
$xmlProtocolado = $protocol->add($xmlAssinado,$protocolo);
```
Por fim usamos o *file_put_contents* para criar um arquivo XML em disco para aguardar essa nota. A receita exige que você guarde os XMLs das suas notas pelo menos por 5 anos, então cuida bem delas.
```php
file_put_contents('nota.xml',$xmlProtocolado);
```

## Conclusão
A ideia com esse passo a passo é dar um ponta pé inicial para quem nunca emitiu uma Nf-e/Nfc-e, mostrando o passo a passo necessário para enviar um nota para receita.
