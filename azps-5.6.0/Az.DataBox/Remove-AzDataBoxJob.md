---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942650"
---
# <span data-ttu-id="409de-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="409de-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="409de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409de-102">SYNOPSIS</span></span>
<span data-ttu-id="409de-103">Az adatdoboz-feladat törlése</span><span class="sxs-lookup"><span data-stu-id="409de-103">Deletes the databox job</span></span>

## <span data-ttu-id="409de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="409de-104">SYNTAX</span></span>

### <span data-ttu-id="409de-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="409de-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409de-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="409de-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409de-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="409de-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="409de-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="409de-108">DESCRIPTION</span></span>
<span data-ttu-id="409de-109">A **Remove-AzDataBox Jobs** parancsmag egy kész adatdoboz-feladat törlésére használható az adatdoboz-feladatok listájából.</span><span class="sxs-lookup"><span data-stu-id="409de-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="409de-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="409de-110">EXAMPLES</span></span>

### <span data-ttu-id="409de-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="409de-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="409de-112">A megadott adatdoboz-feladat törlése</span><span class="sxs-lookup"><span data-stu-id="409de-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="409de-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="409de-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="409de-114">A megadott adatdoboz-feladat végleges törlése jóváhagyás nélkül</span><span class="sxs-lookup"><span data-stu-id="409de-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="409de-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="409de-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="409de-116">A megadott adatdoboz-feladat törlése</span><span class="sxs-lookup"><span data-stu-id="409de-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="409de-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="409de-117">PARAMETERS</span></span>

### <span data-ttu-id="409de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409de-118">-DefaultProfile</span></span>
<span data-ttu-id="409de-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="409de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="409de-120">-Force</span><span class="sxs-lookup"><span data-stu-id="409de-120">-Force</span></span>
<span data-ttu-id="409de-121">Eltávolítás kényszerítés megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="409de-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="409de-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="409de-122">-InputObject</span></span>
<span data-ttu-id="409de-123">InputObject típusú PSDataBoxData</span><span class="sxs-lookup"><span data-stu-id="409de-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409de-124">-Name</span><span class="sxs-lookup"><span data-stu-id="409de-124">-Name</span></span>
<span data-ttu-id="409de-125">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="409de-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409de-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="409de-126">-PassThru</span></span>
<span data-ttu-id="409de-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="409de-127">PassThru</span></span>

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

### <span data-ttu-id="409de-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="409de-128">-ResourceGroupName</span></span>
<span data-ttu-id="409de-129">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="409de-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409de-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="409de-130">-ResourceId</span></span>
<span data-ttu-id="409de-131">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="409de-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="409de-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="409de-132">-Confirm</span></span>
<span data-ttu-id="409de-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="409de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="409de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="409de-134">-WhatIf</span></span>
<span data-ttu-id="409de-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="409de-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="409de-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="409de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="409de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409de-137">CommonParameters</span></span>
<span data-ttu-id="409de-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409de-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="409de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409de-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="409de-140">INPUTS</span></span>

### <span data-ttu-id="409de-141">System.String</span><span class="sxs-lookup"><span data-stu-id="409de-141">System.String</span></span>

## <span data-ttu-id="409de-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="409de-142">OUTPUTS</span></span>

### <span data-ttu-id="409de-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="409de-143">System.Void</span></span>

## <span data-ttu-id="409de-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="409de-144">NOTES</span></span>

## <span data-ttu-id="409de-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="409de-145">RELATED LINKS</span></span>
