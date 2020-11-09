---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298898"
---
# <span data-ttu-id="dce83-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="dce83-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="dce83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dce83-102">SYNOPSIS</span></span>
<span data-ttu-id="dce83-103">A databox feladat törlése</span><span class="sxs-lookup"><span data-stu-id="dce83-103">Deletes the databox job</span></span>

## <span data-ttu-id="dce83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dce83-104">SYNTAX</span></span>

### <span data-ttu-id="dce83-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dce83-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce83-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dce83-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce83-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dce83-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dce83-108">DESCRIPTION</span></span>
<span data-ttu-id="dce83-109">A **Remove-AzDataBoxJob** parancsmag a befejezett databox-feladatok törlésére szolgál a databox-feladatok listájából.</span><span class="sxs-lookup"><span data-stu-id="dce83-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="dce83-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dce83-110">EXAMPLES</span></span>

### <span data-ttu-id="dce83-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dce83-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="dce83-112">A megadott databox-feladat törlése</span><span class="sxs-lookup"><span data-stu-id="dce83-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="dce83-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="dce83-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="dce83-114">A megadott databox-feladat törlése megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="dce83-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="dce83-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="dce83-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="dce83-116">A megadott databox-feladat törlése</span><span class="sxs-lookup"><span data-stu-id="dce83-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="dce83-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dce83-117">PARAMETERS</span></span>

### <span data-ttu-id="dce83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce83-118">-DefaultProfile</span></span>
<span data-ttu-id="dce83-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dce83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dce83-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dce83-120">-Force</span></span>
<span data-ttu-id="dce83-121">Az Eltávolítás kényszerítése megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="dce83-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="dce83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce83-122">-InputObject</span></span>
<span data-ttu-id="dce83-123">InputObject típusú PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="dce83-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="dce83-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dce83-124">-Name</span></span>
<span data-ttu-id="dce83-125">Databox-feladat neve</span><span class="sxs-lookup"><span data-stu-id="dce83-125">Databox Job Name</span></span>

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

### <span data-ttu-id="dce83-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dce83-126">-PassThru</span></span>
<span data-ttu-id="dce83-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="dce83-127">PassThru</span></span>

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

### <span data-ttu-id="dce83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce83-128">-ResourceGroupName</span></span>
<span data-ttu-id="dce83-129">Databox-munka erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="dce83-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="dce83-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dce83-130">-ResourceId</span></span>
<span data-ttu-id="dce83-131">Databox munka erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dce83-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="dce83-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dce83-132">-Confirm</span></span>
<span data-ttu-id="dce83-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dce83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce83-134">-WhatIf</span></span>
<span data-ttu-id="dce83-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dce83-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dce83-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dce83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce83-137">CommonParameters</span></span>
<span data-ttu-id="dce83-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dce83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce83-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dce83-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce83-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce83-140">INPUTS</span></span>

### <span data-ttu-id="dce83-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dce83-141">System.String</span></span>

## <span data-ttu-id="dce83-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce83-142">OUTPUTS</span></span>

### <span data-ttu-id="dce83-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="dce83-143">System.Void</span></span>

## <span data-ttu-id="dce83-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dce83-144">NOTES</span></span>

## <span data-ttu-id="dce83-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dce83-145">RELATED LINKS</span></span>
