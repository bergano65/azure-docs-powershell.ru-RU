---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8db364a6a8842b701e6018fe960d5b29755542a9
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104716750"
---
# Add-AzureAccount

## SYNOPSIS
Добавляет учетную запись Azure в Windows PowerShell.

## СИНТАКСИС

### Пользователь (по умолчанию)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
Благодаря **настройку Add-AzureAccount** ваша учетная запись Azure и ее подписки будут доступны в Windows PowerShell.
Это похоже на вход в учетную запись Azure в Windows PowerShell.
Чтобы выйти из учетной записи, используйте **cmdlet Remove-AzureAccount.**

**Add-AzureAccount** скачивает сведения об учетной записи Azure и сохраняет ее в файле данных подписки в перемещаемом профиле пользователя.
Он также получает маркер доступа, позволяющий Windows PowerShell доступ к учетной записи Azure от вашего имени.
После выполнения команды вы можете управлять своей учетной записью Azure в Windows PowerShell.

Сделать учетную запись Azure доступной для Windows PowerShell можно двумя Windows PowerShell.
Вы можете использовать **cmdlet Add-AzureAccount,** который использует маркеры доступа для проверки подлинности Azure Active Directory (Azure AD) или **Import-AzurePublishSettingsFile,** для которого используется сертификат управления.
Инструкции по использованию см. в инструкциях [по подключению к подписке.](https://azure.microsoft.com/documentation/articles/install-configure-powershell) https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect)

При запуске **Add-AzureAccount** отображается интерактивное окно с запросом на вход в учетную запись Azure.
Этот вход действителен до окончания срока действия маркера доступа.
По истечении этого срока для работы с учетной записью будет предложено снова запустить **add-AzureAccount.**

В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .

## ПРИМЕРЫ

### Пример 1. Добавление учетной записи
```
PS C:\> Add-AzureAccount
```

Эта команда добавляет учетную запись Azure в Windows PowerShell.
При запуске команды появляются окна с запросом имени пользователя и пароля учетной записи.

### Пример 2. Использование альтернативного файла данных подписки
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Эта команда использует параметр **SubscriptionDataFile,** чтобы направлять **Add-AzureAccount** на хранение данных учетной записи в C:\Testing\SDF.xml, а не в файле по умолчанию.

## PARAMETERS

### -Credential
```yaml
Type: PSCredential
Parameter Sets: User
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases:

Required: True
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

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет
Этот cmdlet не может вводиться в канал

## OUTPUTS

### Нет
Этот cmdlet не возвращает результатов.

## ПРИМЕЧАНИЯ
* **Add-AzureAccount** (и метод проверки подлинности Azure AD) имеют приоритет над **import-AzurePublishSettings** (и методом сертификата управления). Если вы используете **Add-AzureAccount** хотя бы один раз в своей учетной записи, используется метод проверки подлинности Azure AD, а сертификат управления игнорируется. Чтобы удалить маркер Azure AD и восстановить метод сертификата управления, используйте **cmdlet Remove-AzureAccount.** Для получения дополнительных сведений введите: **Get-Help Remove-AzureAccount.**
* Ошибка "Срок действия ваших учетных данных истек. Войдите Add-AzureAccount" указывает на то, что срок действия маркера доступа истек и Windows PowerShell не удается получить доступ к учетной записи Azure. Чтобы восстановить доступ к своей учетной записи, снова **запустите Add-AzureAccount.**
* С учетной записью и подпиской Azure PowerShell можно получить данные из файла данных подписки, а не из учетной записи Azure Live. Если вы измените учетную запись или подписки за пределами Windows PowerShell, например с помощью портала управления Azure, снова запустите **Add-AzureAccount,** чтобы обновить файл данных подписки.

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


