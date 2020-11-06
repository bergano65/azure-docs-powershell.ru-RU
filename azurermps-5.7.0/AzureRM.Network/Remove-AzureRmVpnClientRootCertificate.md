---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b86637618b0ef6a2ed337a48d5bdebf8888fad2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570248"
---
# Remove-AzureRmVpnClientRootCertificate

## КРАТКИй обзор
Удаляет существующий корневой сертификат VPN-клиента.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmVpnClientRootCertificate** удаляет указанный корневой сертификат из шлюза виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.
Если удалить корневой сертификат на компьютерах, использующих сертификат для проверки подлинности, подключение к шлюзу станет недоступным.

При использовании **Remove-AzureRmVpnClientRootCertificate** необходимо указать как имя сертификата, так и текстовое представление данных сертификата.
Дополнительные сведения о текстовом представлении сертификата можно найти в описании параметра *PublicCertData* .

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление корневого сертификата клиента из шлюза виртуальной сети
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

В этом примере удаляется корневой сертификат клиента с именем ContosoRootCertificate из шлюза виртуальной сети ContosoVirtualGateway.

Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления сертификата; Это текстовое представление хранится в переменной с именем $Text.

Вторая команда использует цикл for для извлечения всего текста в $Text за исключением первой строки и последней строки.
Извлеченный текст хранится в переменной с именем $CertificateText.

Третья команда использует данные, хранящиеся в переменной $CertificateText, вместе с командлетом **Remove-AzureRmVpnClientRootCertificate** , чтобы удалить сертификат из шлюза.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Указывает текстовое представление корневого сертификата, который нужно удалить.
Чтобы получить текстовое представление, экспортируйте его в формате CER (с использованием Base64), а затем откройте полученный файл в текстовом редакторе.
Результат должен выглядеть примерно так: Обратите внимание на то, что реальный результат будет содержать гораздо больше строк, чем сокращенный образец, показанный ниже.

-----"Начало-----сертификата" MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----

PublicCertData состоит из всех строк между первой строкой (-----"начало-----сертификата") и последней строки (-----конец сертификата-----) в файле.
Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.

Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Указывает имя шлюза виртуальной сети, из которого удаляется сертификат.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Указывает имя корневого сертификата клиента, который удаляет этот командлет.

```yaml
Type: String
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[New-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)


