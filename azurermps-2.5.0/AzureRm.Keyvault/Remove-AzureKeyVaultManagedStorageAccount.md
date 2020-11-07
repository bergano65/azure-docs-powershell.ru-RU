---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913336"
---
# Remove-AzureKeyVaultManagedStorageAccount

## КРАТКИй обзор
Удаляет управляемую учетную запись хранилища Azure с основным хранилищем и все связанные определения SAS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Отменяет связь учетной записи хранения Azure из хранилища ключей. Это не приведет к удалению учетной записи хранения Azure, но удаляет ключи учетной записи из управления с помощью Azure Key Vault. Также удаляются все связанные определения SAS хранилища управляемых хранилищ.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление учетной записи хранения для хранилища ключей, управляемой службой хранилища Azure, и всех связанных определений SAS.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей. Учетная запись "mystorageaccount" не будет удалена. Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.

### Пример 2: Удаление учетной записи хранения для хранилища ключей в службе управления правами и всех связанных определений SAS без подтверждения пользователя.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей. Учетная запись "mystorageaccount" не будет удалена. Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.

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

### -Force
Не запрашивать подтверждение.

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

### -PassThru
По умолчанию командлет не возвращает объект.
Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.

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

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

