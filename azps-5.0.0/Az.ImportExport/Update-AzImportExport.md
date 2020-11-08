---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247799"
---
# Update-AzImportExport

## КРАТКИй обзор
Обновляет определенные свойства задания.
Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.
Она также может использоваться для отмены существующего задания.

## Максимальное

### UpdateExpanded (по умолчанию)
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## NОПИСАНИЕ
Обновляет определенные свойства задания.
Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.
Она также может использоваться для отмены существующего задания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление задания ImportExport по группе ресурсов и имени сервера
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Этот командлет обновляет ImportExport задание по группе ресурсов и имени сервера.

### Пример 2: обновление задания ImportExport по идентификационным данными.
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Этот командлет обновляет ImportExport задание с помощью удостоверения.

## ПАРАМЕТРЫ

### -AcceptLanguage
Указывает предпочтительный язык ответа.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupDriveManifest
Указывает, должны ли файлы манифестов на дисках быть скопированы в блоки больших двоичных объектов.

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

### -CancelRequested
Если задано значение, оно должно быть истинным.
Служба пытается отменить задание.

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

### -DeliveryPackageCarrierName
Имя несущей частоты, используемой для отправки и импорта и экспорта дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageDriveCount
Количество дисков, включенных в пакет.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageShipDate
Дата отгрузки пакета.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageTrackingNumber
Номер отслеживания пакета.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveList
Список дисков, составляющих задание.
Для конструирования ознакомьтесь с разделом "Заметки" для свойств DRIVELIST и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
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
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogLevel
Указывает, включено ли ведение журнала ошибок или подробный журнал.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя задания импорта и экспорта.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCity
Название города, которое будет использоваться при возврате дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCountryOrRegion
Страна или регион, которые нужно использовать при возврате дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressEmail
Адрес электронной почты получателя возвращенных дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressPhone
Номер телефона получателя возвращенных дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressPostalCode
Почтовый индекс, который будет использоваться при возврате дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressRecipientName
Имя получателя, который будет получать жесткие диски при их возвращении.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStateOrProvince
Область или край, которые нужно использовать при возврате дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStreetAddress1
Первая строка почтового адреса, который будет использоваться для возврата дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStreetAddress2
Вторая строка почтового адреса, который будет использоваться для возврата дисков.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnShippingCarrierAccountNumber
Номер счета клиента с перевозчиком.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnShippingCarrierName
Название несущей частоты.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Если задано значение, оно должно быть доставлено, которое сообщает службе импорта и экспорта о том, что пакет для задания отгружен.
Свойства ReturnAddress и DeliveryPackage должны быть заданы либо в этом запросе, либо в предыдущем запросе, в противном случае запрос завершится сбоем.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Идентификатор подписки для пользователя Azure.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Тег
Указывает теги, которые будут назначены заданию

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IJobResponse

## Пуск

СВЯЗЫВАЮТ

СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ

Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.


DRIVELIST <IDriveStatus [] >: список дисков, составляющих задание.
  - `[BitLockerKey <String>]`: Ключ BitLocker, используемый для шифрования диска.
  - `[BytesSucceeded <Int64?>]`: Байты успешно переданы на диск.
  - `[CopyStatus <String>]`: Подробные сведения о состоянии процесса передачи данных. Это поле не возвращается в ответе до тех пор, пока диск не находится в состоянии перепередачи.
  - `[DriveHeaderHash <String>]`: Хэш-значение заголовка диска.
  - `[DriveId <String>]`: Серийный номер оборудования диска без пробелов.
  - `[ErrorLogUri <String>]`: URI, указывающий на большой двоичный объект, который содержит журнал ошибок для операции передачи данных.
  - `[ManifestFile <String>]`: Относительный путь к файлу манифеста на диске. 
  - `[ManifestHash <String>]`: Хэш MD5, закодированный Base16, для файла манифеста на диске.
  - `[ManifestUri <String>]`: URI, указывающий на большой двоичный объект, содержащий файл манифеста диска. 
  - `[PercentComplete <Int32?>]`: Процент завершения для диска. 
  - `[State <DriveState?>]`: Текущее состояние диска. 
  - `[VerboseLogUri <String>]`: URI, указывающий на большой двоичный объект, содержащий подробный журнал для операции передачи данных. 

INPUTOBJECT <IImportExportIdentity> : параметр Identity
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[JobName <String>]`: Имя задания импорта и экспорта.
  - `[LocationName <String>]`: Имя расположения. Например, "Западная США" или "westus".
  - `[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.
  - `[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

