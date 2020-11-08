---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076612"
---
# Get-AzsStorageQuota

## КРАТКИй обзор


## Максимальное

### Список (по умолчанию)
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Получить
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## NОПИСАНИЕ


## ИЛЛЮСТРИРУЮТ

### Пример 1:
```powershell
PS C:\> Get-AzsStorageQuota
```

Получите список квот хранилища.

### Пример 2:
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

Получение сведений об указанной квоте хранилища по имени.

## ПАРАМЕТРЫ

### -DefaultProfile


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

### -InputObject
Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Location


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


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId


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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota



## Пуск

Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.

INPUTOBJECT <IStorageAdminIdentity> : 
  - `[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.
  - `[AsyncOperationId <String>]`: Идентификатор асинхронной операции.
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[Location <String>]`: Расположение ресурса.
  - `[QuotaName <String>]`: Имя дисковой квоты.
  - `[ResourceGroup <String>]`: Имя группы ресурсов.
  - `[ServiceName <String>]`: Имя службы хранилища.
  - `[SubscriptionId <String>]`: Идентификатор подписки.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

