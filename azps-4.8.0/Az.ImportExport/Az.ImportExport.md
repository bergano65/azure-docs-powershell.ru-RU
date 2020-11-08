---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242753"
---
# AZ. ImportExport Module
## Nописание
Командлеты Microsoft Azure PowerShell: ImportExport

## Командлеты AZ. ImportExport
### [Get-AzImportExport](Get-AzImportExport.md)
Получает сведения о существующем задании.

### [Get-AzImportExportBitLockerKey](Get-AzImportExportBitLockerKey.md)
Возвращает ключи BitLocker для всех дисков в указанном задании.

### [Get-AzImportExportLocation](Get-AzImportExportLocation.md)
Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.
Расположение — это регион Azure.

### [New-AzImportExport](New-AzImportExport.md)
Создание нового задания или обновление существующего задания в указанной подписке.

### [New-AzImportExportDriveListObject](New-AzImportExportDriveListObject.md)
Создайте объект DriverList для ImportExport.

### [Remove-AzImportExport](Remove-AzImportExport.md)
Удаление существующего задания.
Удалять можно только задания в состоянии "создать" или "завершено".

### [Update-AzImportExport](Update-AzImportExport.md)
Обновляет определенные свойства задания.
Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.
Она также может использоваться для отмены существующего задания.

