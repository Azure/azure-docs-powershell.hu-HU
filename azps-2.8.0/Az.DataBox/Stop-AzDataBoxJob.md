---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 491d86aa474fb5c392c2d9360657cd1a91072154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667095"
---
# <span data-ttu-id="42cb8-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="42cb8-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="42cb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="42cb8-103">Folyamatban lévő databox-feladat lemondása, ha a feladat visszavonhatatlan állapotban van.</span><span class="sxs-lookup"><span data-stu-id="42cb8-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="42cb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42cb8-104">SYNTAX</span></span>

### <span data-ttu-id="42cb8-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42cb8-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cb8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42cb8-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cb8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42cb8-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42cb8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="42cb8-109">A **stop-AzDataBoxJob** parancsmag a databox-feladatok lemondására szolgál.</span><span class="sxs-lookup"><span data-stu-id="42cb8-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="42cb8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="42cb8-110">EXAMPLES</span></span>

### <span data-ttu-id="42cb8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42cb8-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="42cb8-112">A megadott databox feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="42cb8-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="42cb8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="42cb8-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="42cb8-114">A megadott databox-feladat visszavonása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="42cb8-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="42cb8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="42cb8-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="42cb8-116">A megadott databox feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="42cb8-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="42cb8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42cb8-117">PARAMETERS</span></span>

### <span data-ttu-id="42cb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cb8-118">-DefaultProfile</span></span>
<span data-ttu-id="42cb8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42cb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42cb8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="42cb8-120">-Force</span></span>
<span data-ttu-id="42cb8-121">Kényszerített leállítás megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="42cb8-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="42cb8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42cb8-122">-InputObject</span></span>
<span data-ttu-id="42cb8-123">InputObject típusú PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="42cb8-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="42cb8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42cb8-124">-Name</span></span>
<span data-ttu-id="42cb8-125">Databox-feladat neve</span><span class="sxs-lookup"><span data-stu-id="42cb8-125">Databox Job Name</span></span>

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

### <span data-ttu-id="42cb8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42cb8-126">-PassThru</span></span>
<span data-ttu-id="42cb8-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="42cb8-127">PassThru</span></span>

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

### <span data-ttu-id="42cb8-128">– Ok</span><span class="sxs-lookup"><span data-stu-id="42cb8-128">-Reason</span></span>
<span data-ttu-id="42cb8-129">A lemondás oka</span><span class="sxs-lookup"><span data-stu-id="42cb8-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="42cb8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cb8-130">-ResourceGroupName</span></span>
<span data-ttu-id="42cb8-131">Databox-munka erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="42cb8-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="42cb8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42cb8-132">-ResourceId</span></span>
<span data-ttu-id="42cb8-133">Databox erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="42cb8-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="42cb8-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42cb8-134">-Confirm</span></span>
<span data-ttu-id="42cb8-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42cb8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42cb8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42cb8-136">-WhatIf</span></span>
<span data-ttu-id="42cb8-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42cb8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42cb8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42cb8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42cb8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cb8-139">CommonParameters</span></span>
<span data-ttu-id="42cb8-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42cb8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cb8-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="42cb8-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cb8-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42cb8-142">INPUTS</span></span>

### <span data-ttu-id="42cb8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42cb8-143">System.String</span></span>

## <span data-ttu-id="42cb8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42cb8-144">OUTPUTS</span></span>

### <span data-ttu-id="42cb8-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="42cb8-145">System.Void</span></span>

## <span data-ttu-id="42cb8-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42cb8-146">NOTES</span></span>

## <span data-ttu-id="42cb8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42cb8-147">RELATED LINKS</span></span>
