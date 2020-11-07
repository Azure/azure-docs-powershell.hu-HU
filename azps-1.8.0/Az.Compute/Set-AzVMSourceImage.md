---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: af25c6ef380eaadef8c03ee3c7f1f7b37af77fb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836645"
---
# Set-AzVMSourceImage

## Áttekintés
A virtuális gép képét adja meg.

## SZINTAXISA

### ImageReferenceSkuParameterSet (alapértelmezett)
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImageReferenceIdParameterSet
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzVMSourceImage** parancsmag a virtuális gépekhez használni kívánt platform képét adja meg.

## Példák

### 1. példa: a képek értékeinek beállítása
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.
A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.
A végleges parancs a Publisher-név, az ajánlat, a SKU és a verzió értékeit állítja be.
A **Get-AzVMImagePublisher** , a **Get-AzVMImageOffer** , a Get- **AzVMImageSku** és a Get- **AzVMImage** parancsmagok felfedezhetik ezeket a beállításokat.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Az azonosítót adja meg.

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ajánlat
A VMImage-ajánlat típusát adja meg.
Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
A VMImage közzétevő nevét adja meg.
Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Egy VMImage SKU-ot ad meg.
A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A VMImage verziószámát adja meg.
A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
A konfigurálandó helyi virtuális gép objektumát adja meg.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

### System. String

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Új – AzVMConfig](./New-AzVMConfig.md)


