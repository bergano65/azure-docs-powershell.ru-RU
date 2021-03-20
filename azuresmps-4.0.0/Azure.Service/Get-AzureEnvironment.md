---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d598f22851c054528aefadc12a170ed394a490f4
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104716529"
---
# Get-AzureEnvironment

## SYNOPSIS
Получает среды Azure

## СИНТАКСИС

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **его использованием** получаются среды Azure, доступные для Windows PowerShell.

Среда Azure — независимое развертывание Microsoft Azure, например AzureCloud для глобального azure и AzureChinaCloud для Azure, управляемый компанией 21Vianet в Китае.
Вы также можете создавать локально среды Azure с помощью пакетов Azure и cmdlets WAPack.
Дополнительные сведения см. в [azure Pack).](/previous-versions/azure/windows-server-azure-pack/)

С **использованием cmdlet Get-AzureEnvironment** среды получаются из файла данных подписки, а не Из Azure.
Если файл данных подписки устарел, запустите для обновления файл **Add-AzureAccount** или **Import-PublishSettingsFile.**

В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

## ПРИМЕРЫ

### Пример 1. Получить все среды
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw...
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Эта команда возвращает все среды, доступные для Windows PowerShell.

### Пример 2. Получить среду по имени
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

В этом примере возвращается среда AzureCloud.

### Пример 3. Получить все свойства всех сред
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Эта команда получает все свойства всех сред.

Команда использует командлет **Get-AzureEnvironment** для получения всех сред Azure для этой учетной записи.
Затем он использует командлет **Foreach-Object** для выполнения команды **Get-AzureEnvironment** с параметром **Name** в каждой среде.
Значение параметра **Name** — это свойство **EnvironmentName** каждой среды.

Без параметров **Get-AzureEnvironment** получает только выбранные свойства среды.

## PARAMETERS

### -Name
Возвращает только указанную среду.
Введите имя среды.
Значение параметра в параметрах в конфиденциальном случае.
Поддиавные знаки не разрешены.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet можно ввести по имени свойства, но не по значению.

## OUTPUTS

### System.Management.Automation.PSCustomObject
По умолчанию **Get-AzureEnvironment** возвращает настраиваемый объект.

### Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment
При запуске **Get-AzureEnvironment с** параметром **Name** возвращается объект **WindowsAzureEnvironment.**

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


