---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466492"
---
# Get-AzTemplateSpec

## SYNOPSIS
Sablon specifikációi

## SZINTAXIS

### ListTemplateSpecsParameterSet (alapértelmezett)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Ez a parancsmag használható sablon specifikációk listához egy előfizetés/erőforráscsoportban, vagy egy adott sablon specifikációjának lekérthez név vagy azonosító alapján. Ha egy adott sablont név/azonosító alapján kap meg, a **-Version** paraméterben megadott verziónév megadásával szükség esetén lekérhet egy adott verziót. A **-Version** használata esetén csak az adott verzió részletei lesznek jelen a **verzióban. A visszaadott* Template Spec objektum verziószámai. Ha a Sablon specifikációjának név/azonosító alapján való beolvasásakor nincs megadva adott verzió, az összes verzió a * értéken belül fog *jelenni. A visszaadott* objektum Versions tulajdonsága.

**Megjegyzés:** Amikor egy előfizetés vagy erőforráscsoport összes sablon specifikációját felsorolja, minden egyes visszaadott sablon specifikációja *". A Versions"* tulajdonság *null értékű* lesz. A verzióinformációk csak akkor szerepelnek itt, ha -Name vagy -ResourceId paramétert ad meg (például: egy adott sablon specifikációját/verzióját kéri).

## PÉLDÁK

### 1. példa: Listasablon specifikációi az aktuális előfizetésben
```powershell
PS C:\> Get-AzTemplateSpec
```

Az aktuális előfizetés összes sablon specifikációját felsorolja.

### 2. példa: List Template Specs in a resource group
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Az aktuális előfizetés "myRG" erőforráscsoportjának sablon specifikációit sorolja fel.

### 3. példa: Sablon specifikációjának lekérte (az összes verzióval) név szerint
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Információkat kap a "MyTemplateSpec" nevű sablon specifikációról a "myRG" erőforráscsoporton belül.

**Megjegyzés:** A Sablon specifikációjának összes verziója a *". A visszatérési* objektum Versions " tulajdonsága.

### 4. példa: Sablon specifikációjának (adott verzió) lekérte név szerint
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Információkat kap a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verziójáról a "myRG" erőforráscsoporton belül.

**Megjegyzés:** A *". A visszaadott objektum Versions"* tulajdonsága csak a kért verziót fogja tartalmazni.

### 5. példa: Sablon specifikációjának lekérte (az összes verzióval) erőforrás-azonosító alapján
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Információkat kap a "MyTemplateSpec" nevű sablon specifikációról az előfizetési alazonosító "myRG" \{ erőforráscsoportján \} belül.

**Megjegyzés:** A Sablon specifikációjának összes verziója a *". A visszatérési* objektum Versions " tulajdonsága.

### 6. példa: Sablon specifikációjának (adott verzió) lekérte erőforrás-azonosító szerint
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Információkat kap a "MyTemplateSpec" nevű sablon specifikációjának "v1.0" verziójáról az előfizetési alazonosító "myRG" \{ erőforráscsoportján \} belül.

**Megjegyzés:** A *". A visszaadott objektum Versions"* tulajdonsága csak a kért verziót fogja tartalmazni.

## PARAMETERS

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

### -Name
A sablon specifikációjának neve.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A sablon specifikációjának teljesen minősített erőforrás-azonosítója. Példa: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
A sablon specifikációjának verziója.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
