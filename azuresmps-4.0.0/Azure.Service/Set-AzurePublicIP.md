---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075955"
---
# Set-AzurePublicIP

## КРАТКИй обзор
Добавляет общедоступный IP-адрес виртуальной машине Azure.

## Максимальное

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzurePublicIP** добавляет общедоступный IP-адрес виртуальной машине Azure.
Если вы запускаете этот командлет для существующей виртуальной машины, обновите виртуальную машину для реализации изменений.
Вы можете указать метку доменного имени, чтобы создать соответствующую запись DNS для общедоступного IP-адреса.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление общедоступного IP-адреса для существующей виртуальной машины
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .
Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.
Текущий командлет добавляет ftpip имя общедоступного IP-адреса.
Команда передает виртуальную машину командлету **Update-AzureVM** , который реализует ваши изменения.

### Пример 2: Добавление общедоступного IP-адреса для новой виртуальной машины
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Эта команда создает объект конфигурации виртуальной машины с помощью командлета **New-AzureVMConfig** .
Команда передает этот объект в командлет **Add-AzureProvisioningConfig** , который обеспечивает дополнительную настройку.
Текущий командлет добавляет ftpip имя общедоступного IP-адреса.
Команда передает конфигурацию в командлет **New-AzureVM** , который создает виртуальную машину.

### Пример 3: Добавление общедоступного IP-адреса и метки к существующей виртуальной машине
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .
Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.
Текущий командлет добавляет общедоступные IP-имена ftpip и Label ipname.
Эта команда обновляет виртуальную машину, которая реализует изменения.

### Пример 4: Добавление общедоступного IP-адреса и метки к новой виртуальной машине
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Эта команда создает объект конфигурации виртуальной машины и передает этот объект в **Add-AzureProvisioningConfig** , который предоставляет дополнительные настройки.
Текущий командлет добавляет общедоступные IP-имена ftpip и Label ipname.
Команда создает виртуальную машину.

## ПАРАМЕТРЫ

### -DomainNameLabel
Указывает имя, которое будет использоваться для соответствующей записи DNS для общедоступного IP-адреса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Задает тайм-аут простоя TCP в минутах.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Указывает, как этот командлет отвечает на информационное событие.

Для этого параметра допустимы следующие значения:

- Продолжал
- Игнорируйте
- INQUIRE
- SilentlyContinue
- Остановить
- Рвать

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Указывает переменную данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPName
Указывает общедоступное имя IP-адреса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Указывает виртуальную машину, к которой этот командлет добавляет общедоступный IP-адрес.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. ServiceManagement. Model. IPersistentVM

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


