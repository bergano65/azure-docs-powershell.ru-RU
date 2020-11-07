---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: ed0e0f0ddf42266921113b219d81cfd5b6b6417c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728326"
---
# New-AzWebAppSSLBinding

## КРАТКИй обзор
Создание привязки сертификата SSL для веб-приложения Azure.

## Максимальное

### Состояний
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Режима
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Режим
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzWebAppSSLBinding** создает для веб-приложения Azure Связывание сертификата Secure Socket Layer (SSL).
Командлет создает привязку SSL двумя способами: 
- Вы можете привязать веб-приложение к существующему сертификату.
- Вы можете добавить новый сертификат и затем привязать веб-приложение к этому новому сертификату.
Независимо от того, какой подход вы используете, сертификат и веб-приложение должны быть связаны с одной и той же группой ресурсов Azure.
Если у вас есть веб-приложение в группе ресурсов а и вы хотите привязать это веб-приложение к сертификату в группе ресурсов B, единственным способом является Отправка копии сертификата в группу ресурсов A. Если вы загрузили новый сертификат, имейте в виду следующие требования для SSL-сертификата Azure: 
- Сертификат должен содержать закрытый ключ. 
- Сертификат должен использовать формат почтового обмена личной информацией (PFX). 
- Имя субъекта сертификата должно соответствовать домену, который используется для доступа к веб-приложению. 
- Сертификат должен использовать не менее 2048-битного шифрования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: привязка сертификата к веб-приложению
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Эта команда привязывает существующий сертификат Azure (сертификат с отпечатным E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) к веб-приложению с именем ContosoWebApp.

## ПАРАМЕТРЫ

### -CertificateFilePath
Задает путь к файлу для сертификата, который нужно отправить.
Параметр *CertificateFilePath* требуется только в том случае, если сертификат еще не был загружен в Azure.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Задает пароль для расшифровки сертификата.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Name (имя)
Указывает имя веб-приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен сертификат.
В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Указывает имя слота развертывания веб-приложения.
Вы можете использовать командлет Get-AzWebAppSlot, чтобы получить доступ к ячейкам.
Слоты развертывания предоставляют способ для размещения и проверки веб-приложений без доступа к этим приложениям через Интернет.
Обычно изменения развертываются на промежуточный сайт, проверяют эти изменения, а затем развертываются на рабочем сайте (доступ к Интернету).

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Указывает, включен ли сертификат.
Установите для параметра *SSLState* значение 1, чтобы включить сертификат, или установите для *SSLState* значение 0, чтобы отключить сертификат.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отпечаток
Указывает уникальный идентификатор сертификата.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Указывает веб-приложение.
Чтобы получить веб-приложение, используйте командлет Get-AzWebApp.
Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Указывает имя веб-приложения, для которого создается новая привязка SSL.
В одной команде нельзя использовать параметры *WebAppName* и *webapp* .

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Apps. PSSite

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. website. Models. HostNameSslState

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


