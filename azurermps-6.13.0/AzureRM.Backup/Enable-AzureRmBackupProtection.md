---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c66eda488b0b7876317b02db279202a88bbcc3d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565940"
---
# Enable-AzureRmBackupProtection

## КРАТКИй обзор
Связывает элемент с политикой защиты резервных копий Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Enable-AzureRmBackupProtection** связывает элемент с политикой защиты резервного копирования Azure.
Чтобы включить политику защиты, необходимо сначала создать существующий элемент резервной копии и существующую политику.
Оба должны принадлежать одному хранилищу резервных копий.
Расписание резервного копирования производит полную начальную копию элемента и добавочную копию для последующих резервных копий.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Включение защиты на виртуальной машине Azure
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда сохраняет этот объект в переменной $Vault.
Вторая команда получает политику защиты резервного копирования с именем DefaultPolicy для хранилища в $Vault.
Команда сохраняет этот объект в переменной $Policy.
В последней команде для передачи значений из одного командлета в другой используется оператор конвейера.
Он получает контейнер с помощью командлета Get-AzureRmBackupContainer.
Команда получает элемент резервного копирования из этого контейнера с помощью командлета Get-AzureRmBackupItem.
Текущий командлет включает политику, хранящуюся в $Policy для элемента, который команда передает этому командлету.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Указывает элемент резервного копирования, для которого этот командлет включит защиту.
Чтобы получить **AzureRmBackupItem** , используйте командлет Get-AzureRmBackupItem.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Policy (политика)
Задает политику защиты, которую этот командлет связывает с элементом.
Чтобы получить объект **AzureRmBackupProtectionPolicy** , используйте командлет Get-AzureRmBackupProtectionPolicy.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainerContextObject
Параметры: Item (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


