---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073131"
---
# Invoke-AzStorageSyncCompatibilityCheck

## КРАТКИй обзор
Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.

## Максимальное

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

## NОПИСАНИЕ
Командлет **Invoke-AzStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем с совместимостью между вашей системой и синхронизацией файлов Azure. Если указан локальный или удаленный путь, он выполняет набор проверок пространства имен System и File и возвращает все найденные проблемы совместимости.
Проверки системы:
- Проверки пространства имен файла совместимости ОС:
- Неподдерживаемые символы
- Максимальный размер файла
- Максимальная длина пути
- Максимальная длина файла
- Максимальный размер набора данных
- Максимальная глубина каталога

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA.

### Пример 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Эта команда проверяет совместимость файлов и папок в C:\DATA, но не выполняет проверку совместимости системы.

### Пример 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA, а затем экспортирует результаты в виде CSV-файла для C:\results.

## ПАРАМЕТРЫ

### -ComputerName
Компьютер, на котором вы хотите выполнить эту проверку.

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
Ваши учетные данные для проверяемого общего доступа.

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
UNC-путь к проверяемому общему ресурсу.

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
Установите этот флаг для пропуска проверок пространства имен файлов и только для проверки системы.

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
Установите этот флаг для пропуска системных проверок и выполнения только проверок пространства имен файлов.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## Пуск
* Ключевые слова: Azure, AZ, ARM, Resource, Management, storagesync, FileSync

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
