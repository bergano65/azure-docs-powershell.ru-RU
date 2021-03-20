---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f45e535d5be89ed38ec713438b6a372a755d32b
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104716045"
---
# Set-AzureSubscription

## SYNOPSIS
Изменяет подписку Azure.

## СИНТАКСИС

### UpdateSubscriptionByIdParameterSetName (по умолчанию)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **использованием cmdlet Set-AzureSubscription** можно установить и изменить свойства объекта подписки Azure.
Этот cmdlet можно использовать для работы с подпиской Azure, которая не является используемой по умолчанию подпиской, или для изменения текущей учетной записи хранилища.
Сведения о текущих и стандартных подписках см. в **cmdlet Select-AzureSubscription.**

Этот cmdlet выполняется с объектом Подписки Azure, а не с вашей фактической подпиской На Azure.
Чтобы создать и оформить подписку На Azure, посетите [портал Azure](https://azure.microsoft.com/) https://azure.microsoft.com/) (.

Этот cmdlet изменяет данные в файле данных подписки, который создается при использовании для добавления учетной записи Azure в Windows PowerShell с помощью **add-AzureAccount** или **Import-AzurePublishSettingsFile.**

В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

## ПРИМЕРЫ

### Пример 1. Изменение существующей подписки1
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

В этом примере изменяется сертификат для подписки ContosoEngineering.

### Пример 2. Изменение конечной точки службы
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

Эта команда добавляет или изменяет настраиваемую конечную точку службы для подписки ContosoEngineering.

### Пример 3. Очистка значений свойств
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

Эта команда задает для свойств Certificate и ResourceManagerEndpoint значение NULL ($Null).
При этом значения этих свойств очищаются без изменения других параметров.

### Пример 4. Использование альтернативного файла данных подписки
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

Эта команда изменяет текущую учетную запись хранилища подписки ContosoFinance на ContosoStorage01.
Команда использует параметр **SubscriptionDataFile** для изменения данных в файле данных C:\Azure\SubscriptionData.xml подписки.
По умолчанию **Set-AzureSubscription** использует файл данных подписки по умолчанию в перемещаемом профиле пользователя.

## PARAMETERS

### -Certificate
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Контекст
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Среда
Указывает среду Azure.

Среда Azure — независимое развертывание Microsoft Azure, например AzureCloud для глобального azure и AzureChinaCloud для Azure, управляемый компанией 21Vianet в Китае.
Вы также можете создавать локально среды Azure с помощью пакетов Azure и cmdlets WAPack.
Дополнительные сведения см. в [пакете Azure.](/previous-versions/azure/windows-server-azure-pack/)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает $True, если команда будет успешной, $False если она не будет возвращена.
По умолчанию этот cmdlet не возвращает никаких выходных данных.
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ResourceManagerEndpoint
Указывает конечную точку для данных Диспетчера ресурсов Azure, включая данные о группах ресурсов, связанных с учетной записью.
Дополнительные сведения о диспетчере [](https://go.microsoft.com/fwlink/?LinkID=394765) ресурсов Azure https://go.microsoft.com/fwlink/?LinkID=394765) [](https://go.microsoft.com/fwlink/?LinkID=394767) см. в использовании Windows PowerShell диспетчера ресурсов Azure. https://go.microsoft.com/fwlink/?LinkID=394767)

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

### -ServiceEndpoint
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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases:

Required: True
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

### None или System.Boolean
При использовании *параметра PassThru* этот cmdlet возвращает boolean value.
По умолчанию этот cmdlet не возвращает никаких выходных данных.

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Select-AzureSubscription](./Select-AzureSubscription.md)


