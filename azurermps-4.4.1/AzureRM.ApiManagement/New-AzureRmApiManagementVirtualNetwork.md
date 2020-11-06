---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492614"
---
# New-AzureRmApiManagementVirtualNetwork

## Áttekintés
Létrehozza a PsApiManagementVirtualNetwork példányát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApiManagementVirtualNetwork** parancsmag a **PsApiManagementVirtualNetwork** példányának létrehozására szolgáló segítő parancs.
Ez a parancs a **set-AzureRMApiManagementVirtualNetworks** parancsmaggal használható.

## Példák

### Példa 1: virtuális hálózat létrehozása
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

Ez a példa virtuális hálózatot hoz létre, majd felhívja a **set-AzureRmApiManagementVirtualNetworks** parancsmagot.

## PARAMÉTEREK

### -Hely
Annak a virtuális hálózatnak a helyét adja meg, amelyben ez a parancsmag létrehozta a példányt.

A paraméter elfogadható értékei a következők:

- Közép-amerikai Észak-amerikai
- Dél-Közép-amerikai
- Közép-amerikai
- Nyugat-Európa
- Észak-Európa
- Nyugat-amerikai
- Kelet-amerikai
- Kelet-amerikai 2
- Japán (kelet)
- Japán West
- Dél-Brazília
- Dél-ázsiai
- Kelet-ázsiai
- Ausztrália – Kelet
- Ausztrália délkeleti

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetResourceId
A virtuális hálózat alhálózati erőforrás-AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

