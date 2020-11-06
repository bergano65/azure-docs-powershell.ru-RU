---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 820a1c84600a3fb143d2b3c34a81e1f7cedac0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570404"
---
# Add-AzureKeyVaultManagedStorageAccount

## КРАТКИй обзор
Добавляет существующую учетную запись хранилища Azure в заданное хранилище ключей для ключей, управляемых службой хранилища ключей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Настройка существующей учетной записи хранилища Azure с хранилищем ключей для ключей учетной записи хранения для управления с помощью ключей. Учетная запись хранения уже должна существовать. Ключи хранилища никогда не открываются для вызывающего абонента.
Автоматическое повторное создание ключа и переключение активного ключа на основе периода повторного создания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка учетной записи хранения Azure с помощью ключа Vault для управления ее ключами
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Задает учетной записи хранения с основным хранилищем ключей для управления с помощью Key Vault. Для активного ключа задано значение "key1". Этот ключ будет использоваться для создания маркеров SAS. Ключевое приложение получит повторное создание ключа "key2" после периода повторного создания с момента выполнения этой команды и задает его в качестве активного ключа. Этот процесс автоматического повторного создания продолжится между "key1" и "key2" с пропуском в 90 дней.

### Пример 2: Настройка классической учетной записи хранилища Azure с помощью ключа Vault для управления ее ключами
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Задает классический учетной записи хранилища с основным хранилищем ключей для управления с помощью Key Vault. Активным является параметр "основной". Этот ключ будет использоваться для создания маркеров SAS. Ключевое приложение получит повторное создание ключа "дополнительный" после периода повторного создания с момента этой команды и установит его в качестве активного ключа. Этот процесс автоматического повторного создания продолжится между "основным" и "дополнительным" с пропуском в 90 дней.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Имя учетной записи хранилища с управляемым хранилищем. Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
Идентификатор ресурса Azure учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Имя ключа учетной записи хранения, которое необходимо использовать для создания маркеров SAS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отключение
Отключение использования ключа управляемой учетной записи хранения для создания маркеров SAS.

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

### -DisableAutoRegenerateKey
Автоматическое повторное создание ключа. Если установлено значение true, неактивный ключ для управляемой учетной записи хранения будет автоматически восстановлен и станет новым активным ключом после периода повторного создания. Если задано значение false, ключи управляемой учетной записи хранения не воссоздаются автоматически.

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

### -RegenerationPeriod
Период повторного создания. Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets управляемой учетной записи хранилища становится новым активным ключом.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Имя хранилища.
Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
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

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[AzureRM.KeyVault](/powershell/module/azurerm.keyvault)
