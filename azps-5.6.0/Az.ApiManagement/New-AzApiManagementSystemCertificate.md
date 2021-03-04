---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: cc3cc5d0e7ae617fc745c2f119f7da9df88417a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959192"
---
# New-AzApiManagementSystemCertificate

## SYNOPSIS
Создает экземпляр `PsApiManagementSystemCertificate` . Сертификат может быть выдан частным ЦС и будет установлен в службе управления API в `CertificateAuthority` или `Root` магазине.

## СИНТАКСИС

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **New-AzApiManagementSystemCertificate** является командлетом-помощником, который создает экземпляр **PsApiManagementSystemCertificate.**
Эта команда используется с New-AzApiManagement и Set-AzApiManagement командлетом.

## ПРИМЕРЫ

### Пример 1. Создание и инициализация экземпляра PsApiManagementSystemCertificate с помощью SSL-сертификата из файла
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

Эта команда создает и инициализирует экземпляр **PsApiManagementSystemCertificate с** помощью корневого сертификата ЦС. Затем создается служба управления API, которая устанавливает сертификат ЦС в корневой магазин.

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

### -PfxPassword
Пароль для файла сертификата PFX.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPath
Путь к файлу сертификата PFX.

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

### -StoreName
Имя Магазина сертификатов

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Security.SecureString

## OUTPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzApiManagement](./New-AzApiManagement.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)