---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492597"
---
# Remove-AzureRmApiManagementRegion

## Áttekintés
Eltávolítja a meglévő központi telepítő régiót a PsApiManagement-példányból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmApiManagementRegion** parancsmag a **Microsoft. Azure. commands. ApiManagement. models. PsApiManagementRegion** fájltípust eltávolítja egy **AdditionalRegions** -gyűjteményből, a **Microsoft. Azure. commands. ApiManagement. modellek. PsApiManagement**.
Ez a parancsmag nem módosítja magát a központi telepítőt, de frissíti a **PsApiManagement** -példányt a memóriában.
Az API-menedzsment telepített példányának frissítéséhez adja át a módosított **PsApiManagementInstance** a **Update-AzureRmApiManagement**.

## Példák

### 1. példa: régió eltávolítása PsApiManagement példányból
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Ez a parancs eltávolítja a kelet-amerikai régiót a **PsApiManagement** példányból.

### 2. példa: régió eltávolítása PsApiManagement példányból parancsok sorozatával
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Az első parancs az **PsApiManagement** példányát kapja a contoso nevű ContosoApi nevű erőforráscsoport nevében.
A végleges parancs ezután eltávolítja a kelet-amerikai régiót az adott példányból, majd frissíti a bevezetést.

## PARAMÉTEREK

### -ApiManagement
Azt a **PsApiManagement** -példányt adja meg, amelyre a parancsmag eltávolítja a további központi terjesztési területet.

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

### -Hely
A parancsmag által eltávolított régió helyét adja meg.

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
Accept pipeline input: True (ByPropertyName)
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

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


