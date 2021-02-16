---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146090"
---
# Get-AzADSpCredential

## SYNOPSIS
Beolvassa a szolgáltatásnévvel társított hitelesítő adatok listáját.

## SZINTAXIS

### ObjectIdParameterSet (alapértelmezett)
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNObjectParameterSet
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A Get-AzADSpCredential parancsmaggal lekérheti a szolgáltatásnévvel társított hitelesítő adatok listáját.
Ez a parancs beolvassa a szolgáltatásnévvel társított összes hitelesítőadat-tulajdonságot (de a hitelesítő adatokat nem).

## PÉLDÁK

### 1. példa : Hitelesítő adatok felsorolása SPN szerint

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

Visszaadja az egyszerű szolgáltatásnévhez tartozó hitelesítő adatok listáját az SPN " http://test12345 ".

### 2. példa: A hitelesítő adatok listába sorolása objektumazonosító alapján

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

A "58e28616-99cc-4da4-b705-7672130e1047" objektumazonosítóval társított egyszerű szolgáltatáshoz tartozó hitelesítő adatok listáját adja eredményül.

### 3. példa : A hitelesítő adatok felsorolása pipázás használatával

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

A "58e28616-99cc-4da4-b705-7672130e1047" objektumazonosítóval beszerzúdő egyszerű szolgáltatásnév, és a Get-AzADSpCredential-parancsmagba való beömlődve felsorolja az adott egyszerű szolgáltatásnévhez szükséges összes hitelesítő adatokat.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -DisplayName
A szolgáltatásnév megjelenítendő neve

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
A szolgáltatásnév objektumazonosítója, amelyből a hitelesítő adatokat lekéri.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
A szolgáltatásnév (SPN) neve, amelyből a hitelesítő adatokat beolvassa.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
A hitelesítő adatok beolvasására használt egyszerű szolgáltatásobjektum.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

## KIMENETEK

### Microsoft.Azure.Commands.ActiveDirectory.PSADCredential

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

