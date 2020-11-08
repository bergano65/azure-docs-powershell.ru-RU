---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076564"
---
# Get-AzureSiteRecoveryVaultSettingsFile

## КРАТКИй обзор
Получает файл параметров хранилища для восстановления сайта.

## Максимальное

### ByParam (по умолчанию)
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByObject
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSiteRecoveryVaultSettingsFile** получает файл параметров для хранилища Azure Site Recovery.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение файла параметров для хранилища
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

Первая команда получает активное хранилище Azure Site Recovery с именем ContosoVault с помощью командлета **Get-AzureSiteRecoveryVault** .
Команда сохраняет это хранилище в переменной $Vault.

Вторая команда получает файл параметров для хранилища, хранящегося в $Vault.

## ПАРАМЕТРЫ

### -Location
Указывает географическое расположение, в которое входит хранилище.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя хранилища.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Задает путь к файлу параметров хранилища для восстановления сайта.
Чтобы сохранить этот файл на локальном компьютере, скачайте его с портала хранилища сайтов для восстановления сайта после завершения работы команды.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

### -Site
Указывает сайт, для которого нужно получить файл параметров.
Чтобы получить объект **сайта** , используйте командлет **Get-AzureSiteRecoverySite** .

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID сайта
Указывает идентификатор сайта.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteName
Указывает имя сайта.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище для сайта.

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureSiteRecoverySite](./Get-AzureSiteRecoverySite.md)

[Get-AzureSiteRecoveryVault](./Get-AzureSiteRecoveryVault.md)

[Get-AzureSiteRecoveryVaultSettings](./Get-AzureSiteRecoveryVaultSettings.md)

[Import-AzureSiteRecoveryVaultSettingsFile](./Import-AzureSiteRecoveryVaultSettingsFile.md)


