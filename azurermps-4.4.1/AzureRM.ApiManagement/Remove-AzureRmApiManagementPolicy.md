---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492607"
---
# Remove-AzureRmApiManagementPolicy

## Áttekintés
Eltávolítja az API-kezelési házirendet egy megadott hatókörből.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Bérlői szint (alapértelmezett)
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Termékek szintje
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### API-szint
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Műveleti szint
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmApiManagementPolicy** parancsmag meghatározott hatókörből ELTÁVOLÍTJA az API-kezelési házirendet.

## Példák

### 1. példa: a bérlői szintű házirend eltávolítása
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

Ez a parancs eltávolítja a bérlői szintű házirendet az API-menedzsmentből.

### 2. példa: a termékskála-házirend eltávolítása
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

Ez a parancs az API-kezelésből eltávolítja a termékskála-házirendet.

### 3. példa: az API-scope-házirend eltávolítása
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

Ez a parancs eltávolítja az API-scope-házirendet az API-menedzsmentből.

### 4. példa: a műveleti hatókörű házirend eltávolítása
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

Ez a parancs eltávolítja a műveleti hatóköri házirendet az API-kezelésből.

## PARAMÉTEREK

### -ApiId
Egy meglévő API azonosítóját adja meg.
Ha ezt a paramétert adja meg, a parancsmag eltávolítja az API-scope-házirendet.

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
A **PsApiManagementContext** objektum példányát adja meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationId
Egy meglévő művelet azonosítóját adja meg.
Ha a *ApiId* paraméterrel adja meg ezt a paramétert, ez a parancsmag eltávolítja a művelet-hatóköri házirendet.

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Termékkód
A meglévő szorzat azonosítóját adja meg.
Ha ezt a paramétert adja meg, a parancsmag eltávolítja a Product-scope-házirendet.

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### Logikai

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Set-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)


