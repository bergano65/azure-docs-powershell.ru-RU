---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076396"
---
# Add-AzureAccount

## КРАТКИй обзор
Добавление учетной записи Azure в Windows PowerShell.

## Максимальное

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

## NОПИСАНИЕ
Командлет **Add-AzureAccount** делает учетную запись Azure и ее подписки доступными в Windows PowerShell.
Это напоминает вход в учетную запись Azure в Windows PowerShell.
Чтобы выйти из учетной записи, используйте командлет **Remove-AzureAccount** .

**Add-AzureAccount** загружает сведения о своей учетной записи Azure и сохраняет ее в файле данных подписки в перемещаемом профиле пользователя.
Кроме того, он получает маркер доступа, который позволяет Windows PowerShell получить доступ к учетной записи Azure от вашего имени.
После завершения команды вы можете управлять учетной записью Azure в Windows PowerShell.

Учетную запись Azure можно сделать доступной для Windows PowerShell двумя разными способами.
Вы можете использовать командлет **Add-AzureAccount** , который использует маркеры доступа для проверки подлинности Azure Active Directory (Azure AD) или **Import-AzurePublishSettingsFile** , который использует сертификат управления.
Рекомендации по использованию этого метода приведены [в статье инструкции: подключение к подписке](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

При запуске **Add-AzureAccount** открывается интерактивное окно с запросом на вход в учетную запись Azure.
Этот вход будет действителен, пока не истечет срок действия маркера доступа.
По истечении срока действия командлетов, которым требуется доступ к вашей учетной записи, будет выдать запрос на повторный запуск **надстройки AzureAccount** .

В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление учетной записи
```
PS C:\> Add-AzureAccount
```

Эта команда добавляет учетную запись Azure в Windows PowerShell.
При выполнении команды появляется всплывающее окно с запросом имени пользователя и пароля учетной записи.

### Пример 2: использование альтернативного файла данных подписки
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Эта команда использует параметр **SubscriptionDataFile** для прямого **добавления AzureAccount** для хранения данных учетной записи в C:\Testing\SDF.xml файле вместо файла по умолчанию.

## ПАРАМЕТРЫ

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

### -Environment
Указывает среду Azure.

Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.
Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.
Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -Клиент
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Вы не можете передавать входные данные в этот командлет

## НАПРЯЖЕНИЕ

### Ничего
Этот командлет не возвращает никаких выходных данных.

## Пуск
* **Надстройка Add-AzureAccount** (и метод проверки подлинности Azure AD) имеет приоритет над параметрами **Import-AzurePublishSettings** (и способом сертификации управления). Если вы используете команду **Add-AzureAccount** даже один раз в своей учетной записи, используется метод проверки подлинности Azure AD, и сертификат управления пропускается. Чтобы удалить маркер Azure AD и восстановить метод сертификата управления, используйте командлет **Remove-AzureAccount** . Для получения дополнительных сведений введите: **Get-Help Remove-AzureAccount**.
* Ошибка "срок действия ваших учетных данных истек. Для повторного входа используйте Add-AzureAccount. срок действия маркера доступа истек, и Windows PowerShell не может получить доступ к учетной записи Azure. Чтобы восстановить доступ к учетной записи, запустите **надстройку Add-AzureAccount** еще раз.
* Учетная запись и командлеты подписки Azure PowerShell получают данные из файла данных подписки, а не из действующей учетной записи Azure. Если вы изменяете учетную запись или подписки за пределами Windows PowerShell, например с помощью портала управления Azure, запустите **Add-AzureAccount** еще раз, чтобы обновить файл данных подписки.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


