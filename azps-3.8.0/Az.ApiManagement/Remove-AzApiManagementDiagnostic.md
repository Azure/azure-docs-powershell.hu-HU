---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 309e306b4f7049241ba6a1ce83f60ea977b9e08f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012226"
---
# Remove-AzApiManagementDiagnostic

## Áttekintés
A diagnosztikai entitás eltávolítása globális vagy API-szintű hatókörből

## SZINTAXISA

### ByResourceIdParameterSet (alapértelmezett)
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExpandParameterSetName
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectParameterSet
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A parancsmag **eltávolítása – AzApiManagementDiagnostic** eltávolítja a `DiagnosticId` globális hatókörből vagy hatókörből megadott diagnosztikai entitást. `ApiId`

## Példák

### 1. példa: a diagnosztikai entitás eltávolítása
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

Ez a példa eltávolítja az `applicationinsights` API-menedzsment szolgáltatás diagnosztikai szolgáltatását.

## PARAMÉTEREK

### -ApiId
Az API-azonosító.
Ehhez a paraméterhez szükség van.

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
A PsApiManagementContext példánya.
Ehhez a paraméterhez szükség van.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DiagnosticId
A meglévő szorzat azonosítója
Ha meg van adva a termékek hatókörét visszaadó házirend.
Ez a paraméter nem kötelező.

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
A PsApiManagementDiagnostic példánya. Ehhez a paraméterhez szükség van.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Ha a megadott művelet sikeres, akkor a True Write True értékre vált.
Ez a paraméter nem kötelező.

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

### -ResourceId
A kar ResourceId diagnosztikai nézete. Ehhez a paraméterhez szükség van.

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzApiManagementDiagnostic](./Get-AzApiManagementDiagnostic.md)

[Új – AzApiManagementDiagnostic](./New-AzApiManagementDiagnostic.md)

[Set-AzApiManagementDiagnostic](./Set-AzApiManagementDiagnostic.md)