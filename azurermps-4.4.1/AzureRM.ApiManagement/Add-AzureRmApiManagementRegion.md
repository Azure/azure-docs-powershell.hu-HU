---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503320"
---
# Add-AzureRmApiManagementRegion

## Áttekintés
Új központi terjesztési régiók felvétele egy PsApiManagement-példányba.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmApiManagementRegion** parancsmag a **PsApiManagementRegion** új példányát adja a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagement** **AdditionalRegions** példányának.
Ez a parancsmag nem telepíti magát semmit, de a memória **PsApiManagement** példányát frissíti.
Az API-menedzsment telepített példányának frissítéséhez a módosított **PsApiManagement** -példányt a Update-AzureRmApiManagementDeployment-ra kell átadni.

## Példák

### 1. példa: új központi terjesztési régiók felvétele PsApiManagement-példányba
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Ez a parancs két prémium SKU-egységet és a kelet-amerikai régiót a **PsApiManagement** -példányra helyezi.

### 2. példa: új üzembe állítási régiók felvétele PsApiManagement-példányba, majd a központi telepítő frissítése
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

Ez a parancs **PsApiManagement** objektumot kap, és két prémium SKU-egységet ad hozzá a kelet-amerikai régióhoz, majd frissíti a központi üzembe helyezést.

## PARAMÉTEREK

### -ApiManagement
Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag további központi terjesztési területeket ad.

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
A központi telepítő terület SKU-kapacitását adja meg.

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

### -Hely
Az új központi terjesztési terület helyét adja meg.

Az érvényes értékek a következők: 

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

### -SKU
A központi telepítő terület küszöbértékét adja meg.
Az érvényes értékek a következők: 

- Fejlesztő
- Standard
- Prémium verzió

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

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

### PsApiManagement
A ' ApiManagement ' paraméter az "PsApiManagement" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagement

## MEGJEGYZI
* A parancsmag frissített **PsApiManagement** -példányt ír a pipeline-ra.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)


