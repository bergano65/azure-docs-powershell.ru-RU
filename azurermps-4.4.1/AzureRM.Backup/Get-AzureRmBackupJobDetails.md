---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560531"
---
# Get-AzureRmBackupJobDetails

## КРАТКИй обзор
Получает сведения о задании резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### JobsFiltersSet (по умолчанию)
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFiltersSet
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupJobDetails** получает сведения о задании резервного копирования Azure.
Вы можете использовать этот командлет для сбора сведений о неуспешном выполнении задания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: отображение сведений о невыполненном задании
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает сбойные задания из хранилища в $Vault, а затем сохраняет их в переменной массива $Jobs.

Третье задание получает сведения для первого задания в переменной $Jobs и затем сохраняет эти сведения в переменной $JobDetails.

Последняя команда отображает свойство **ErrorDetails** для $JobDetails с помощью стандартного синтаксиса с точкой.

### Пример 2: отображение рекомендуемого действия для невыполненного задания
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

Эта команда отображает рекомендуемое действие из переменной $JobDetails, созданной в первом примере.

## ПАРАМЕТРЫ

### -Job
Указывает задание, для которого этот командлет получает сведения.
Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания, сведения о котором этот командлет получает.
Идентификатор — это свойство **InstanceId** объекта **AzureRmBackupJob** .
Чтобы получить объект **AzureRmBackupJob** , используйте Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, для которого этот командлет получает сведения о задании.
Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
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

### Ничего

## НАПРЯЖЕНИЕ

### AzureRmBackupJobDetails

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


