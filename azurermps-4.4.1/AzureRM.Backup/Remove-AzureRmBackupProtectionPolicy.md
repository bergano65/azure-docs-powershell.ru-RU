---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565666"
---
# Remove-AzureRmBackupProtectionPolicy

## КРАТКИй обзор
Удаление политики из резервного хранилища.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmBackupProtectionPolicy** удаляет политику из хранилища резервных копий Azure.

Прежде чем можно будет удалить политику защиты резервных копий, она не должна содержать ни одного связанного элемента резервного копирования.
Перед удалением политики убедитесь, что все связанные элементы связаны с какой – либо другой политикой.
Чтобы связать другую политику с элементом резервной копии, используйте командлет Enable-AzureRmBackupProtection.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление политики защиты резервной копии
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.
Команда сохраняет этот объект в переменной $Vault.

Вторая команда создает политику хранения в течение 30 дней ежедневной сохранности, а затем сохраняет ее в переменной $Daily.

Вторая команда получает политику защиты с именем DailyBackup в хранилище в $Vault с помощью командлета **Get-AzureRmBackupProtectionPolicy** .
Команда передает политику текущему командлету.
Этот командлет удаляет политику.

## ПАРАМЕТРЫ

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -ProtectionPolicy
Задает политику защиты, которую удаляет этот командлет.
Чтобы получить **AzureRmBackupProtectionPolicy** , используйте командлет Get-AzureRmBackupProtectionPolicy

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### AzureRMBackupProtectionPolicy

## НАПРЯЖЕНИЕ

### Ничего

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


