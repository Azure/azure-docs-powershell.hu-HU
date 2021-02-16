---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144291"
---
# <span data-ttu-id="3a55c-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="3a55c-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="3a55c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a55c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a55c-103">Eltávolítja az adat megosztást.</span><span class="sxs-lookup"><span data-stu-id="3a55c-103">Removes a data share.</span></span>

## <span data-ttu-id="3a55c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a55c-104">SYNTAX</span></span>

### <span data-ttu-id="3a55c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a55c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a55c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a55c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a55c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a55c-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a55c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a55c-108">DESCRIPTION</span></span>
<span data-ttu-id="3a55c-109">A **Remove-AzDataShare** parancsmag eltávolítja az adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="3a55c-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="3a55c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a55c-110">EXAMPLES</span></span>

### <span data-ttu-id="3a55c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3a55c-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3a55c-112">Ez a parancs eltávolítja az AdsShare nevű adatmegosztást a WikiAds Azure-adatmegosztási fiókból.</span><span class="sxs-lookup"><span data-stu-id="3a55c-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="3a55c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a55c-113">PARAMETERS</span></span>

### <span data-ttu-id="3a55c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a55c-114">-AccountName</span></span>
<span data-ttu-id="3a55c-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="3a55c-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3a55c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a55c-116">-AsJob</span></span>
<span data-ttu-id="3a55c-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3a55c-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3a55c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a55c-118">-DefaultProfile</span></span>
<span data-ttu-id="3a55c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a55c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a55c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a55c-120">-InputObject</span></span>
<span data-ttu-id="3a55c-121">Azure data share object' ''yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="3a55c-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="3a55c-122">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis</span><span class="sxs-lookup"><span data-stu-id="3a55c-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3a55c-123">-Name</span></span>
<span data-ttu-id="3a55c-124">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="3a55c-124">Azure data share name</span></span>

<span data-ttu-id="3a55c-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="3a55c-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="3a55c-126">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis</span><span class="sxs-lookup"><span data-stu-id="3a55c-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a55c-127">-PassThru</span></span>
<span data-ttu-id="3a55c-128">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="3a55c-128">Return object (if specified).</span></span>

<span data-ttu-id="3a55c-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliass:</span><span class="sxs-lookup"><span data-stu-id="3a55c-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="3a55c-130">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="3a55c-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a55c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a55c-132">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="3a55c-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="3a55c-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="3a55c-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="3a55c-134">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: False Accept helyettesítő karakterek: Hamis</span><span class="sxs-lookup"><span data-stu-id="3a55c-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a55c-135">-ResourceId</span></span>
<span data-ttu-id="3a55c-136">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3a55c-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="3a55c-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="3a55c-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="3a55c-138">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (ByPropertyName) Fogadja el a helyettesítő karaktereket: False</span><span class="sxs-lookup"><span data-stu-id="3a55c-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a55c-139">-Confirm</span></span>
<span data-ttu-id="3a55c-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3a55c-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="3a55c-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span><span class="sxs-lookup"><span data-stu-id="3a55c-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="3a55c-142">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="3a55c-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a55c-143">-WhatIf</span></span>
<span data-ttu-id="3a55c-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3a55c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a55c-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a55c-145">The cmdlet is not run.</span></span>

<span data-ttu-id="3a55c-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliass: wi</span><span class="sxs-lookup"><span data-stu-id="3a55c-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="3a55c-147">Kötelező: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span><span class="sxs-lookup"><span data-stu-id="3a55c-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="3a55c-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="3a55c-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="3a55c-149">Kötelező: Igaz pozíció: Elnevezett alapértelmezett érték: Nincs elfogadás folyamatbemenet: Igaz (Érték) Fogadja el a helyettesítő karaktereket: Hamis</span><span class="sxs-lookup"><span data-stu-id="3a55c-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="3a55c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a55c-150">CommonParameters</span></span>
<span data-ttu-id="3a55c-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a55c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a55c-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a55c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a55c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a55c-153">INPUTS</span></span>

### <span data-ttu-id="3a55c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="3a55c-154">System.String</span></span>

### <span data-ttu-id="3a55c-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3a55c-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3a55c-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a55c-156">OUTPUTS</span></span>

### <span data-ttu-id="3a55c-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a55c-157">System.Boolean</span></span>

## <span data-ttu-id="3a55c-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a55c-158">NOTES</span></span>

## <span data-ttu-id="3a55c-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a55c-159">RELATED LINKS</span></span>
