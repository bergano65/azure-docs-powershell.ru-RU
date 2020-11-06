---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 941be726f2b7c7aaf3ebf3d4cef0a91239e88214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559632"
---
# New-AzureRmVpnClientRootCertificate

## КРАТКИй обзор
Создание нового корневого сертификата VPN-клиента.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmVpnClientRootCertificate** создает новый корневой сертификат VPN для использования на шлюзе виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.

Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.
Вместо этого сертификат, созданный с помощью **New-AzureRmVpnClientRootCertificate** , используется вместе с командлетом New-AzureRmVirtualNetworkGateway при создании нового шлюза.
Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.
Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.
Например,

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

Дополнительные сведения можно найти в документации по командлету New-AzureRmVirtualNetworkGateway.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание корневого сертификата aclient
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

В этом примере создается корневой сертификат клиента и сохраняется объект сертификата в переменной с именем $Certificate.
Эта переменная может затем использоваться командлетом **New-AzureRmVirtualNetworkGateway** для добавления корневого сертификата в новый шлюз виртуальной сети.

Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления корневого сертификата; текстовые данные хранятся в переменной с именем $Text.

Вторая команда использует цикл for, чтобы извлечь весь текст, кроме первой строки и последней строки, сохранив извлеченный текст в переменной с именем $CertificateText.

Третья команда использует командлет **New-AzureRmVpnClientRootCertificate** , чтобы создать сертификат, сохранив созданный объект в переменной с именем $Certificate.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя для нового корневого сертификата клиента.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Указывает текстовое представление корневого сертификата, который нужно добавить.
Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.
На экран будет выведено сообщение (Обратите внимание на то, что реальный вывод содержит гораздо больше строк, чем сокращенный образец, показанный ниже).

-----"Начало-----сертификата" MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----

PublicCertData состоит из всех строк между первой строкой (-----"начало-----сертификата") и последней строки (-----конец сертификата-----) в файле.
Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Этот командлет не поддерживает конвейерный вход.

## НАПРЯЖЕНИЕ

###  
Этот командлет создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


