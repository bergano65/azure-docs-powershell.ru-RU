---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559355"
---
# Get-AzureRmBackupContainer

## КРАТКИй обзор
Получает контейнеры резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmBackupContainer** получает контейнеры архивации Azure.

**AzureBackupContainer** инкапсулирует источники данных, защищенные элементы и точки восстановления.
**AzureBackupContainer** может принимать одно из следующих значений: 

- Компьютер с Windows Server
- Сервер System Center Data Protection Manager (SCDPM) 
- Инфраструктура Azure в качестве виртуальной машины службы (IaaS)

Перед тем, как резервное копирование может создать резервную копию источника данных или элемента, необходимо зарегистрировать контейнер, содержащий его в службе архивации Azure.
Для отправки резервных данных в резервное хранилище необходимо проверить подлинность контейнера.
Для компьютеров с Windows Server и серверов SCDPM регистрация удерживается с полным доменным именем сервера.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Просмотр всех серверов, зарегистрированных в хранилище
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает все контейнеры типа Windows из хранилища в $Vault.

### Пример 2: получение определенного контейнера
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Эта команда получает контейнер с именем DPMSERVER. CONTOSO.COM.
Команда задает хранилище в $Vault и тип контейнера.

### Пример 3: Просмотр всех зарегистрированных виртуальных машин Azure
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Эта команда получает зарегистрированные виртуальные машины из хранилища в $Vault.

## ПАРАМЕТРЫ

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

### -ManagedResourceGroupName
Указывает имя группы ресурсов, связанной с контейнером.
Это имя совпадает со значением, которое вы указали для параметра *ServiceName* или *ResourceGroupName* командлета Register-AzureRmBackupContainer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя контейнера, который получает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Указывает текущее состояние контейнеров, которые получает этот командлет.
Для этого параметра допустимы следующие значения:

- NotRegistered 
- Пользователь 
- Регистрируя

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип контейнеров, которые получает этот командлет.

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Указывает хранилище резервных копий, из которого этот командлет получает контейнеры.
Чтобы получить **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### AzureBackupVault

## НАПРЯЖЕНИЕ

### AzureBackupContainer

## Пуск
* Ничего

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Регистрация — AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Отмена регистрации — AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


