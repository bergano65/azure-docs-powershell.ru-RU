---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075932"
---
# New-AzureCertificateSetting

## КРАТКИй обзор
Создание объекта параметров сертификата для сертификата — служба.

## Максимальное

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureCertificateSetting** создает объект параметра сертификата для сертификата, который находится в службе Azure.

Вы можете использовать объект параметров сертификата для создания объекта конфигурации с помощью командлета **Add-AzureProvisioningConfig** .
Используйте объект конфигурации для создания виртуальной машины с помощью командлета **New-AzureVM** .
Вы можете использовать объект параметров сертификата для создания виртуальной машины с помощью командлета **New-AzureQuickVM** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта параметров сертификата
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Эта команда создает объект параметра сертификата для существующего сертификата.

### Пример 2: создание виртуальной машины, использующей объект параметров конфигурации
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Первая команда добавляет сертификат ContosoCert. cer в службу с именем ContosoService с помощью командлета **Add-AzureCertificate** .

Вторая команда создает объект параметра сертификата и сохраняет его в переменной $CertificateSetting.

Третья команда получает изображение из репозитория изображений с помощью командлета **Get-AzureVMImage** .
Эта команда хранит изображение в переменной $Image.

Последняя команда создает объект конфигурации виртуальной машины на основе изображения в $Image с помощью командлета **New-AzureVMConfig** .
Команда передает этот объект командлету **Add-AzureProvisioningConfig** с помощью оператора конвейера.
Этот командлет добавляет данные подготовки в конфигурацию.
Команда передает объект в командлет **New-AzureVM** , который создает виртуальную машину.

## ПАРАМЕТРЫ

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

### -Столбец StoreName
Указывает хранилище сертификатов, в которое нужно добавить сертификат.
Допустимые значения: 

- AddressBook
- AuthRoot
- CertificateAuthority
- Запрещены
- Настроек
- Узла
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Отпечаток
Указывает отпечаток сертификата.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


