---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155899"
---
# <span data-ttu-id="8df2d-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8df2d-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="8df2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8df2d-103">Megszakít egy folyamatban lévő adatdoboz-feladatot, ha a feladat megszakítható állapotban van.</span><span class="sxs-lookup"><span data-stu-id="8df2d-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="8df2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8df2d-104">SYNTAX</span></span>

### <span data-ttu-id="8df2d-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8df2d-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df2d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df2d-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8df2d-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8df2d-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df2d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8df2d-108">DESCRIPTION</span></span>
<span data-ttu-id="8df2d-109">A **Stop-AzDataBox Job** parancsmag egy adatdoboz-feladat megszakítására használható.</span><span class="sxs-lookup"><span data-stu-id="8df2d-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="8df2d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8df2d-110">EXAMPLES</span></span>

### <span data-ttu-id="8df2d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8df2d-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="8df2d-112">A megadott adatdoboz-feladat megszakítása</span><span class="sxs-lookup"><span data-stu-id="8df2d-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="8df2d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8df2d-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="8df2d-114">A megadott adatdoboz-feladat visszavonása jóváhagyás nélkül, kényszerítve</span><span class="sxs-lookup"><span data-stu-id="8df2d-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="8df2d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8df2d-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="8df2d-116">A megadott adatdoboz-feladat megszakítása</span><span class="sxs-lookup"><span data-stu-id="8df2d-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="8df2d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8df2d-117">PARAMETERS</span></span>

### <span data-ttu-id="8df2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df2d-118">-DefaultProfile</span></span>
<span data-ttu-id="8df2d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8df2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df2d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8df2d-120">-Force</span></span>
<span data-ttu-id="8df2d-121">Kényszerített leállítás megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="8df2d-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="8df2d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8df2d-122">-InputObject</span></span>
<span data-ttu-id="8df2d-123">InputObject típusú PSDataBoxData</span><span class="sxs-lookup"><span data-stu-id="8df2d-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="8df2d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8df2d-124">-Name</span></span>
<span data-ttu-id="8df2d-125">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="8df2d-125">Databox Job Name</span></span>

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

### <span data-ttu-id="8df2d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8df2d-126">-PassThru</span></span>
<span data-ttu-id="8df2d-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="8df2d-127">PassThru</span></span>

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

### <span data-ttu-id="8df2d-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="8df2d-128">-Reason</span></span>
<span data-ttu-id="8df2d-129">Lemondás oka</span><span class="sxs-lookup"><span data-stu-id="8df2d-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df2d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df2d-130">-ResourceGroupName</span></span>
<span data-ttu-id="8df2d-131">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="8df2d-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="8df2d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8df2d-132">-ResourceId</span></span>
<span data-ttu-id="8df2d-133">Databox Resource Id</span><span class="sxs-lookup"><span data-stu-id="8df2d-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="8df2d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8df2d-134">-Confirm</span></span>
<span data-ttu-id="8df2d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8df2d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df2d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df2d-136">-WhatIf</span></span>
<span data-ttu-id="8df2d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8df2d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8df2d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8df2d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df2d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df2d-139">CommonParameters</span></span>
<span data-ttu-id="8df2d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df2d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df2d-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8df2d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df2d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8df2d-142">INPUTS</span></span>

### <span data-ttu-id="8df2d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8df2d-143">System.String</span></span>

## <span data-ttu-id="8df2d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8df2d-144">OUTPUTS</span></span>

### <span data-ttu-id="8df2d-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="8df2d-145">System.Void</span></span>

## <span data-ttu-id="8df2d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8df2d-146">NOTES</span></span>

## <span data-ttu-id="8df2d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8df2d-147">RELATED LINKS</span></span>
