---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679336"
---
# Remove-AzureRmADServicePrincipal

## Áttekintés
Az Azure Active Directory Service Principal törlése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Azure Active Directory Service Principal törlése

## Példák

### --------------------------Törölje a AAD.  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

Törli a megadott Azure Active Directory-szolgáltatót.

## PARAMÉTEREK

### -Force
{{Fill Force Description}}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
A törlendő szolgáltató objektum azonosítója.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## KIMENETEK

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[Remove-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)
