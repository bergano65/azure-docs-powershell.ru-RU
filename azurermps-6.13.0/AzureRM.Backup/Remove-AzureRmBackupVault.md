---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561160"
---
# Remove-AzureRmBackupVault

## КРАТКИй обзор
Удаление резервного хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmBackupVault** удаляет хранилище архивации Azure.
Перед удалением резервного хранилища оно должно быть пустым.
С помощью командлета **Remove-AzureRmBackupContainer** удалите инфраструктуру в качестве данных резервной копии виртуальных машин (IaaS) для службы хранилища.
С помощью командлета **delete-registeredserver** можно удалить другие зарегистрированные серверы и данные резервного копирования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление хранилища резервных копий Azure
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

Эта команда получает хранилище резервных копий Azure с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда передает это хранилище в текущий командлет с помощью оператора конвейера.
Текущий командлет удаляет хранилище.

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

### -Force
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, которое удаляет этот командлет.
Чтобы получить **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Параметры: хранилище (ByValue)

## НАПРЯЖЕНИЕ

### System. void

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


