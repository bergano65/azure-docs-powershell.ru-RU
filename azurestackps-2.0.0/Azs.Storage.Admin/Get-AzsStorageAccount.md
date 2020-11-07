---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910482"
---
# Get-AzsStorageAccount

## КРАТКИй обзор
Возвращает запрашиваемую учетную запись хранения.

## Максимальное

### Список (по умолчанию)
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## NОПИСАНИЕ
Возвращает запрашиваемую учетную запись хранения.

## ИЛЛЮСТРИРУЮТ

### Пример 1:
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

Получение списка учетных записей хранения (сводка).

### Пример 2:
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

Получите список учетных записей хранения с подробными сведениями и напечатайте состояние.

### Пример 3:
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

Получение сведений об указанной учетной записи хранения.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Фильтр
Строка фильтра

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Location
Расположение ресурса.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (имя)
Внутренний идентификатор учетной записи хранилища, невидимый для клиента.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Идентификатор подписки.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Сводка
Выберите, следует ли вернуть сводную или подробную информацию.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageAccount



## Пуск

Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.

INPUTOBJECT <IStorageAdminIdentity> : параметр Identity
  - `[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.
  - `[AsyncOperationId <String>]`: Идентификатор асинхронной операции.
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[Location <String>]`: Расположение ресурса.
  - `[QuotaName <String>]`: Имя дисковой квоты.
  - `[ResourceGroup <String>]`: Имя группы ресурсов.
  - `[ServiceName <String>]`: Имя службы хранилища.
  - `[SubscriptionId <String>]`: Идентификатор подписки.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

