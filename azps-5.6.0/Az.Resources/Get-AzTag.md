---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939417"
---
# Get-AzTag

## SYNOPSIS
Előre definiált Azure-címkéket | Egy erőforrás vagy előfizetés teljes címkéit beveszi.

## SZINTAXIS

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS

**GetPredefinedTagSet:** A **Get-AzTag** parancsmag előre definiált Azure-címkéket kap az előfizetésében.
Ez a parancsmag alapvető információkat ad vissza a címkékről vagy a címkékről és azok értékeiről.
Minden kimeneti objektum tartalmaz egy Count tulajdonságot, amely azt jelzi, hogy hány erőforrásra és erőforráscsoportra alkalmazta a címkéket és értékeket.
Az Azure Címkék modul, amely a **Get-AzTag** része, segíthet az előre definiált Azure-címkék kezelésében.
Az Azure-címkék olyan névérték-párok, amelyek segítségével kategorizálhatja Azure-erőforrásait és erőforráscsoportját, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokra és csoportokra vonatkozó megjegyzéseket vagy megjegyzéseket.
Egyetlen lépésben definiálhat és alkalmazhat címkéket, az előre definiált címkékkel azonban szabványos, egységes, kiszámítható neveket és értékeket határozhat meg az előfizetésében szereplő címkékhez.
Előre definiált címke létrehozásához használja a New-AzTag parancsmagot.
Ha előre definiált címkét szeretne alkalmazni  egy erőforráscsoportra, használja a New-AzTag címke paraméterét.
Ha egy adott címkenevet vagy nevet és értéket  keres az erőforráscsoportokban, használja a Get-AzResourceGroup parancsmag címke paraméterét.

**GetByResourceIdParameterSet:** A **ResourceId** azonosítóval elérhető **Get-AzTag** parancsmag a címkék teljes készletét megkapja egy erőforráson vagy előfizetésen.

## PÉLDÁK

### 1. példa: Az összes előre definiált címke betekintése
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Ez a parancs az előfizetésben előre definiált összes címkét megkapja.
A Darab tulajdonság azt mutatja, hogy hányszor lett alkalmazva a címke az előfizetésben található erőforrásokra és erőforráscsoportokra.

### 2. példa: Címke lekérte név szerint
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Ez a parancs részletes információkat kap a Részleg címkéről és annak értékeiről.
A Darab tulajdonság azt mutatja, hogy hányszor lett alkalmazva a címke és annak értékei az előfizetésben található erőforrásokra és erőforráscsoportokra.

### 3. példa: Az összes címke értékeinek lekérte
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Ez a parancs a Részletes *paraméter* segítségével részletes információkat kap az előfizetésben előre definiált címkékről.
A Részletes *paraméter* használata egyenértékű azzal, ha a *Name* paramétert minden címkéhez használja.

### 4. példa: Az előfizetéshez beállított összes címke lekérte

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Ez a parancs a(z) {subId} azonosítóval az előfizetés összes címkéjéhez be lesz állítva.

### 5. példa: Az erőforráshoz beállított címkék teljes készletének be szereznie

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Ez a parancs a(z) {resourceId} segítségével az erőforrás összes címkéjéhez be lesz állítva.

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

### -Részletes
Azt jelzi, hogy ez a művelet információt ad a címkeértékekkel kapcsolatban a kimenethez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Az előre definiált címke neve.
A **Get-AzTag** alapértelmezés szerint alapvető információkat kap az előfizetésben előre definiált címkékről.
A Név paraméter *megadásakor* a *Részletes* paraméternek nincs hatása.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A címkézett entitás erőforrás-azonosítója. Előfordulhat, hogy egy erőforrás, erőforráscsoport vagy előfizetés meg van címkézve.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
