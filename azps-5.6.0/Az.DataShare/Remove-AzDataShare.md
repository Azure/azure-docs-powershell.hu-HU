---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924978"
---
# <span data-ttu-id="a03da-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="a03da-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="a03da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a03da-102">SYNOPSIS</span></span>
<span data-ttu-id="a03da-103">Eltávolítja az adat megosztást.</span><span class="sxs-lookup"><span data-stu-id="a03da-103">Removes a data share.</span></span>

## <span data-ttu-id="a03da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a03da-104">SYNTAX</span></span>

### <span data-ttu-id="a03da-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a03da-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03da-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03da-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03da-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03da-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a03da-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a03da-108">DESCRIPTION</span></span>
<span data-ttu-id="a03da-109">A **Remove-AzDataShare** parancsmag eltávolítja az adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="a03da-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="a03da-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a03da-110">EXAMPLES</span></span>

### <span data-ttu-id="a03da-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a03da-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a03da-112">Ez a parancs eltávolítja az AdsShare nevű adatmegosztást a WikiAds Azure-adatmegosztási fiókból.</span><span class="sxs-lookup"><span data-stu-id="a03da-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="a03da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a03da-113">PARAMETERS</span></span>

### <span data-ttu-id="a03da-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a03da-114">-AccountName</span></span>
<span data-ttu-id="a03da-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="a03da-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03da-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a03da-116">-AsJob</span></span>
<span data-ttu-id="a03da-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a03da-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a03da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03da-118">-DefaultProfile</span></span>
<span data-ttu-id="a03da-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a03da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a03da-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a03da-120">-InputObject</span></span>
<span data-ttu-id="a03da-121">Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a03da-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="a03da-122">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis</span><span class="sxs-lookup"><span data-stu-id="a03da-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a03da-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a03da-123">-Name</span></span>
<span data-ttu-id="a03da-124">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="a03da-124">Azure data share name</span></span>

<span data-ttu-id="a03da-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a03da-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="a03da-126">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis</span><span class="sxs-lookup"><span data-stu-id="a03da-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03da-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a03da-127">-PassThru</span></span>
<span data-ttu-id="a03da-128">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="a03da-128">Return object (if specified).</span></span>

<span data-ttu-id="a03da-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliass:</span><span class="sxs-lookup"><span data-stu-id="a03da-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="a03da-130">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a03da-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a03da-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03da-131">-ResourceGroupName</span></span>
<span data-ttu-id="a03da-132">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="a03da-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="a03da-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a03da-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="a03da-134">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis</span><span class="sxs-lookup"><span data-stu-id="a03da-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03da-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a03da-135">-ResourceId</span></span>
<span data-ttu-id="a03da-136">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a03da-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="a03da-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a03da-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="a03da-138">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (ByPropertyName) Fogadja el a helyettesítő karaktereket: Hamis</span><span class="sxs-lookup"><span data-stu-id="a03da-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a03da-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a03da-139">-Confirm</span></span>
<span data-ttu-id="a03da-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a03da-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="a03da-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span><span class="sxs-lookup"><span data-stu-id="a03da-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="a03da-142">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a03da-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a03da-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03da-143">-WhatIf</span></span>
<span data-ttu-id="a03da-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a03da-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03da-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a03da-145">The cmdlet is not run.</span></span>

<span data-ttu-id="a03da-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliass: wi</span><span class="sxs-lookup"><span data-stu-id="a03da-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="a03da-147">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="a03da-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="a03da-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="a03da-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="a03da-149">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis</span><span class="sxs-lookup"><span data-stu-id="a03da-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="a03da-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03da-150">CommonParameters</span></span>
<span data-ttu-id="a03da-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03da-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03da-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a03da-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03da-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a03da-153">INPUTS</span></span>

### <span data-ttu-id="a03da-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a03da-154">System.String</span></span>

### <span data-ttu-id="a03da-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a03da-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a03da-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a03da-156">OUTPUTS</span></span>

### <span data-ttu-id="a03da-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a03da-157">System.Boolean</span></span>

## <span data-ttu-id="a03da-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a03da-158">NOTES</span></span>

## <span data-ttu-id="a03da-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a03da-159">RELATED LINKS</span></span>
