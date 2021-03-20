---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd1c687005821daa7c779d6bb3db7bbad53c0e28
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104715560"
---
# Set-AzureEnvironment

## SYNOPSIS
Изменяет свойства среды Azure.

## СИНТАКСИС

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его использованием** можно изменить свойства среды Azure.
Она возвращает объект, который представляет среду новыми значениями свойств.
Используйте параметр **Name,** чтобы определить среду, а другие параметры для изменения значений свойств.
Изменить имя среды Azure с помощью **Set-AzureEnvironment** невозможно.

Среда Azure — независимое развертывание Microsoft Azure, например AzureCloud для глобального azure и AzureChinaCloud для Azure, управляемый компанией 21Vianet в Китае.
Вы также можете создавать локально среды Azure с помощью пакетов Azure и cmdlets WAPack.
Дополнительные сведения см. в [пакете Azure.](/previous-versions/azure/windows-server-azure-pack/)

ПРИМЕЧАНИЕ. Не изменяя свойства сред AzureCloud или AzureChinaCloud.
Используйте этот cmdlet для изменения значений в закрытых средах, которые вы создаете.

## ПРИМЕРЫ

### Пример 1. Изменение свойств среды
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

Эта команда изменяет значения свойств **PublishSettingsFileUrl** и **StorageEndpoint** среды ContosoEnv.

## PARAMETERS

### -ActiveDirectoryEndpoint
Изменяет конечную точку проверки подлинности Azure Active Directory на указанное значение.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Определяет ИД ресурса для API управления, доступ которого управляется Azure Active Directory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdTenant
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultDnsSuffix
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultServiceEndpointResourceId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableAdfsAuthentication
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Изменяет конечную точку коллекции диспетчера ресурсов Azure на указанное значение.
Конечная точка коллекции — это расположение для шаблонов коллекции ресурсов.
Дополнительные сведения о группах ресурсов и шаблонах коллекции Azure см. в разделе справки [для Get-AzureResourceGroupGalleryTemplate.](https://go.microsoft.com/fwlink/?LinkID=393052)

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
Изменяет URL-адрес портала управления Azure на указанное значение.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Определяет меняемую среду.
Этот параметр является required(обязательно).
Значение параметра в параметрах в конфиденциальном случае.
Поддиавные знаки не разрешены.

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

### -Profile
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishSettingsFileUrl
Изменяет URL-адрес файлов параметров публикации в указанной среде.
Файл параметров публикации Azure — это XML-файл, содержащий сведения о вашей учетной записи и сертификат управления, позволяющий Windows PowerShell войти в учетную запись Azure от вашего имени.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceManagerEndpoint
Изменение конечной точки для данных Диспетчера ресурсов Azure, включая данные о группах ресурсов, связанных с учетной записью.
Дополнительные сведения о диспетчере [](https://go.microsoft.com/fwlink/?LinkID=394765) ресурсов Azure https://go.microsoft.com/fwlink/?LinkID=394765) [](https://go.microsoft.com/fwlink/?LinkID=394767) см. в использовании Windows PowerShell диспетчера ресурсов Azure. https://go.microsoft.com/fwlink/?LinkID=394767)

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Изменяет URL-адрес конечной точки службы Azure в указанной среде.
Конечная точка службы Azure определяет, управляет ли ваше приложение глобальной платформой Azure, службой Azure, которая управляется компанией 21Vianet в Китае, или частной установкой Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpoint
Изменяет конечную точку по умолчанию для служб хранилища в указанной среде.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)


