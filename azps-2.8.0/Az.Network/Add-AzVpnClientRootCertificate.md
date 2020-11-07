---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 1a38c55757f96b99a6801452f490f0fc4240fde1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903050"
---
# Add-AzVpnClientRootCertificate

## КРАТКИй обзор
Добавляет корневой сертификат VPN-клиента.

## Максимальное

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzVpnClientRootCertificate** добавляет корневой сертификат в шлюз виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации.
По дизайну все сертификаты, используемые на шлюзе, доверяют корневому сертификату.
Этот командлет назначает существующий сертификат как корневой сертификат шлюза.
Если у вас нет сертификата X. 509, вы можете создать его с помощью инфраструктуры открытых ключей или использовать генератор сертификатов, например makecert.exe.
Чтобы добавить корневой сертификат, необходимо указать имя сертификата и предоставить текстовое представление сертификата (Подробнее об этом можно узнать в параметре *PublicCertData* ).
Azure позволяет назначать шлюзу более одного корневого сертификата.
Множественные корневые сертификаты часто развертываются организациями, которые включают пользователей из нескольких компаний.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление корневого сертификата клиента на виртуальный шлюз
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

В этом примере добавляется корневой сертификат клиента на виртуальный шлюз с именем ContosoVirtualGateway.
Первая команда использует командлет **Get-Content** для получения ранее экспортированного текстового представления корневого сертификата и сохраняет эти текстовые данные переменной с именем $text.
Вторая команда использует цикл for для извлечения всего текста за исключением первой строки и последней строки.
Извлеченный текст хранится в переменной с именем $CertificateText.
Третья команда затем использует текст, хранящийся в $CertificateText, с помощью командлета **Add-AzVpnClientRootCertificate** , чтобы добавить корневой сертификат в шлюз.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Указывает текстовое представление корневого сертификата, который нужно добавить.
Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.
В этом случае вывод будет выглядеть примерно так, как показано ниже (Обратите внимание на то, что фактический вывод содержит много строк текста, чем сокращенный образец, показанный здесь):-----начало-----сертификата MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----PublicCertData состоит из всех строк, находящихся между первой строкой (-----начинать сертификат-----) и последней строкой (-----конечный сертификат-----) в файле.
Эти данные можно получить с помощью команд Windows PowerShell, подобных приведенным ниже. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен корневой сертификат.
Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.

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

### -VirtualNetworkGatewayName
Указывает имя шлюза виртуальной сети, в который добавляется сертификат.

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

### -VpnClientRootCertificateName
Указывает имя корневого сертификата клиента, который добавляет этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


