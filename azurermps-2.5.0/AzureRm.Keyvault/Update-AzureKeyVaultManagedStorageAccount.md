---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 2d2e1ff127ce5d355831131c6e366712efee1c29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913868"
---
# Update-AzureKeyVaultManagedStorageAccount

## КРАТКИй обзор
Обновление редактируемых атрибутов хранилища ключей управляемой учетной записи хранилища Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Обновите редактируемые атрибуты хранилища ключей управляемой учетной записи хранения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Обновление активного ключа на "key2" в учетной записи хранения для хранилища ключей, управляемой хранилищем Azure.
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

Обновление активного ключа учетной записи хранения для управляемого хранилища Azure Key на "key2". После этого обновления будет использован "key2" для создания маркеров SAS.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Имя учетной записи хранилища с управляемым хранилищем. Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Имя активного ключа.
Если не указано, существующее значение активного имени ключа управляемой учетной записи хранения останется прежним.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoRegenerateKey
Автоматическое повторное создание ключа.
Если не указано, существующее значение автоматического повторного создания ключа для управляемой учетной записи хранения не изменяется

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable (включить)
Если параметр указан, включает использование управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно true. Отключение использования управляемого ключа учетной записи хранения для создания маркеров SAS, если значение равно false. Если не указано, существующее значение состояния Enabled и Disabled для учетной записи хранения не будет изменено.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
По умолчанию командлет не возвращает объект. Если указан этот параметр, возвращают управляемый объект учетной записи хранения.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegenerationPeriod
Период повторного создания. Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets для управляемой учетной записи хранилища становится активной клавишей. Если не указано, существующее значение периода повторного создания ключей управляемой учетной записи хранения остается неизменным

```yaml
Type: TimeSpan
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
Type: Hashtable
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
