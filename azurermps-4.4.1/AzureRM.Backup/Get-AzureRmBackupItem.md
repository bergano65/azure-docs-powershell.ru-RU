---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559948"
---
# Get-AzureRmBackupItem

## КРАТКИй обзор
Получает элементы в контейнере в резервной копии.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupItem** получает элементы в контейнере в резервной копии Azure и состояние защиты элементов.
Включите элементы для защиты с помощью командлета Enable-AzureRmBackupProtection.

Контейнер, который регистрируется в хранилище резервных копий, может содержать один или несколько элементов, которые можно защитить.
Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение элементов в контейнере
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета **Get-AzureRmBackupContainer** .
Команда сохраняет этот объект в переменной $Container.

Последняя команда получает элемент резервного копирования из контейнера в $Container.

### Пример 2: Просмотр всех свойств элемента
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

Эта команда возвращает элемент резервного копирования в контейнере в $Container, а затем передает его в командлет Select-Object.
Этот командлет возвращает все свойства элемента резервного копирования.
Для получения дополнительных сведений введите `Get-Help Select-Object` .

## ПАРАМЕТРЫ

### -Container
Указывает объект-контейнер, для которого этот командлет получает элементы резервного копирования.
Чтобы получить **AzureRmBackupContainer** , используйте командлет Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionStatus
Определяет общее состояние защиты элемента в контейнере.
Для этого параметра допустимы следующие значения:

- Защищенного 
- Обеспечения  
- NotProtected

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Задает состояние резервного копирования для элемента.
Допустимые значения этого параметра: IRPending, protected, ProtectionError и ProtectionStopped.
Если параметр *ProtectionStatus* имеет значение protected, вы можете использовать значение параметра *Status* для фильтрации элементов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип элемента, который получает этот командлет.
В настоящее время единственным поддерживаемым значением является значение AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

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

### AzureRmBackupContainer

## НАПРЯЖЕНИЕ

### AzureRmBackupItem

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Disable-AzureRmBackupProtection](./Disable-AzureRmBackupProtection.md)

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Restore-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


