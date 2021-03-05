---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005907"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Удаляет существующий корневой сертификат клиента VPN.

## СИНТАКСИС

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для **удаления из** виртуального сетевого шлюза удаляется указанный корневой сертификат.
Корневые сертификаты — это сертификаты X.509, которые определяют корневой сертификат сертификации: все остальные сертификаты, используемые на шлюзе, доверять корневому сертификату.
Если удалить корневой сертификат, компьютеры, на которые он используется в целях проверки подлинности, больше не смогут подключаться к шлюзу.
При использовании **Remove-AzVpnClientRootCertificate** необходимо предоставить как имя сертификата, так и текстовое представление данных сертификата.
Дополнительные сведения о текстовом представлении сертификата см. в описании параметра *PublicCertData.*

## ПРИМЕРЫ

### Пример 1. Удаление корневого сертификата клиента из виртуального сетевого шлюза
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

В этом примере корневой сертификат клиента с именем ContosoRootCertificate удаляется из виртуального сетевого шлюза ContosoVirtualGateway.
Первая команда использует **командлет Get-Content** для получения ранее экспортируемого текстового представления сертификата; Это текстовое представление хранится в переменной с именем $Text.
Затем с помощью циклов вторая команда извлекает весь текст в $Text кроме первой и последней строк.
Извлеченный текст сохраняется в переменной с именем $CertificateText.
В третьей команде используются данные, хранимые в переменной $CertificateText, а также командлет **Remove-AzVpnClientRootCertificate,** чтобы удалить сертификат со шлюза.

## PARAMETERS

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
Указывает текстовое представление корневого сертификата, который нужно удалить.
Чтобы получить текстовое представление, экспортировать сертификат в формате CER (с использованием базовой 64-й кодиации), а затем откройте получивающийся файл в текстовом редакторе.
Результаты должны быть примерно такие же (обратите внимание, что фактический результат будет содержать намного больше строк текста, чем показано в сокращенном примере): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HGUNEW8343NMJklo0 Конечный сертификат -----СVFAw8w ----- PublicCertData состоит из всех линий между первой строкой (----- BEGIN CERTIFICATE -----) и последней строкой (----- END CERTIFICATE -----) в файле.
Получить PublicCertData можно с помощью команд Windows PowerShell примерно так: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Имя группы ресурсов, назначенной виртуальному сетевому шлюзу.
Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.

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
Указывает имя виртуального сетевого шлюза, из которого удален сертификат.

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
Указывает имя корневого сертификата клиента, который удаляет этот cmdlet.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


