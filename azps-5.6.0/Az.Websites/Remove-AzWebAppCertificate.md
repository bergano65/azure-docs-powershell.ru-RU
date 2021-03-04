---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981720"
---
# Remove-AzWebAppCertificate

## SYNOPSIS
Удаляет сертификат, управляемый службой Приложений для Azure Web App. 

## СИНТАКСИС

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Remove-AzWebAppCertificate** удаляется управляемый сертификат Azure App Service Managed.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

Эта команда удаляет сертификат App Service Managed для данного веб-приложения.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThumbPrint
Thumbprint of the certificate that already exists in web space.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
[New-AzWebAppCertificate](./New-AzWebAppCertificate.md)
