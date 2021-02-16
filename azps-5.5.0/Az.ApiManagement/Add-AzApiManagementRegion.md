---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155011"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Új telepítési régiók hozzáadása a PsApiManagement-példányhoz.

## SZINTAXIS

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzApiManagementRegion** parancsmag hozzáadja a **PsApiManagementRegion** új példányát a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement** típusú megadott példány **AdditionalRegions** gyűjteményéhez.
Ez a parancsmag nem telepít semmit önmagában, de frissíti a **PsApiManagement** in-memory példányát.
Egy API-kezelés telepítésének frissítéséhez át kell adni a **módosított PsApiManagement-példányt** a Set-AzApiManagementnek.

## PÉLDÁK

### 1. példa: Új telepítési régiók hozzáadása a PsApiManagement-példányhoz
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Ez a parancs hozzáad két prémium termékváltozatot és a Kelet-US régiót a **PsApiManagement példányhoz.**

### 2. példa: Új telepítési régiók hozzáadása a PsApiManagement-példányhoz, majd a telepítés frissítése
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

Ez a parancs egy **PsApiManagement** objektumot kap, hozzáad két prémium termékváltozatot az EGYESÜLT Államok keleti régiója számára, majd frissíti az üzembe helyezést.

## PARAMETERS

### -ApiManagement
Azt a **PsApiManagement-példányt** adja meg, amelybe ez a parancsmag további telepítési régiókat ad hozzá.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapacitás
A telepítési régió termékváltozatának kapacitását határozza meg.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Location
Megadja az új telepítési régió helyét az Api Management szolgáltatás támogatott régiója között.
Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek

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

### -Termékváltozat
Az üzembe helyezési régió rétegét határozza meg.
Érvényes értékek: 
- Fejlesztő
- Normál
- Prémium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Virtuális hálózati konfigurációt ad meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## KIMENETEK

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## MEGJEGYZÉSEK
* A parancsmag a frissített **PsApiManagement-példányt** folyamatba írja.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)


