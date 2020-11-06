---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565767"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## КРАТКИй обзор
Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### PathBased (по умолчанию)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Invoke-AzureRmStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем с совместимостью между вашей системой и синхронизацией файлов Azure. Если указан локальный или удаленный путь, он выполняет набор проверок пространства имен System и File и возвращает все найденные проблемы совместимости.
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
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA.

### Пример 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Эта команда проверяет совместимость файлов и папок в C:\DATA, но не выполняет проверку совместимости системы.

### Пример 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
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

### -Quiet
Отключает вывод отчета о выводе на консоль.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, storagesync, FileSync

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
