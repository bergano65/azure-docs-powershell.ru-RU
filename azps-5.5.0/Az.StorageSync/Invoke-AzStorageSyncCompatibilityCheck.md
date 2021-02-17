---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231521"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Проверяет наличие возможных проблем совместимости между системой и службой Azure File Sync.

## СИНТАКСИС

### PathBased (по умолчанию)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## ОПИСАНИЕ
Командалет **Invoke-AzStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем совместимости между системой и синхронизацией файлов Azure. Если задан локальный или удаленный путь, выполняется набор проверки системы и пространства имен файлов, которые затем возвращаются все проблемы совместимости.
Системные проверки.
- Проверка пространства имен файлов совместимости ОС:
- Неподтверченные символы
- Максимальный размер файла
- Максимальная длина пути
- Максимальная длина файла
- Максимальный размер наборов данных
- Максимальная глубина каталога

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Эта команда проверяет совместимость системы, а также файлов и папок в папке C:\DATA.

### Пример 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Эта команда проверяет совместимость файлов и папок в папках C:\DATA, но не выполняет проверку совместимости системы.

### Пример 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Эта команда проверяет совместимость системы, а также файлов и папок в папках C:\DATA, а затем экспортирует результаты в C:\results в C:\Results.

## PARAMETERS

### -ComputerName
Компьютер, на который вы выполняете эту проверку.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Ваши учетные данные для подавлимой акции.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
UNC-путь к подавлиемой акции.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
Установите этот флажок, чтобы пропустить проверки пространства имен файлов и выполнять только системные проверки.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Установите этот флажок, чтобы пропустить системные проверки и выполнять только проверки пространства имен файлов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, Az, arm, resource, management, storagesync, filesync

## СВЯЗАННЫЕ ССЫЛКИ
