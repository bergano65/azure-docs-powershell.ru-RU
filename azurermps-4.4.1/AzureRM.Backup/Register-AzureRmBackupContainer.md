---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565668"
---
# Register-AzureRmBackupContainer

## КРАТКИй обзор
Регистрирует контейнер в хранилище резервных копий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Register-AzureRmBackupContainer** регистрирует контейнер в хранилище резервных копий Azure.
Чтобы настроить архивацию с помощью резервной копии Azure, сначала Зарегистрируйте сервер или виртуальную машину в резервном хранилище.
Этот командлет регистрирует инфраструктуру в качестве виртуальной машины службы (IaaS) в указанном хранилище.
Операция регистрации связывает виртуальную машину Azure с резервным хранилищем и отслеживает виртуальную машину в течение жизненного цикла резервного копирования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: регистрация виртуальной машины в резервном хранилище
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.
Команда хранит хранилище в переменной $Vault.

Вторая команда регистрирует виртуальную машину с именем Contoso03Vm с хранилищем в $Vault.
Виртуальная машина принадлежит службе с именем ContosoService27.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя виртуальной машины, зарегистрированной этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов для виртуальной машины.

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Указывает имя службы виртуальной машины, зарегистрированной этим командлетом.

Обычно имя облачной службы имеет суффикс. cloudapp.net.
Не включайте суффикс при указании этого параметра.

Чтобы получить сведения о виртуальной машине, используйте командлет Get-AzureRMVM.
Имя службы — это свойство **DeploymentName** объекта виртуальной машины.

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, на которое этот командлет регистрирует виртуальную машину.
Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRmBackupVault

## НАПРЯЖЕНИЕ

### AzureRmBackupJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


