---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298181"
---
# <span data-ttu-id="471b7-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="471b7-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="471b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="471b7-102">SYNOPSIS</span></span>
<span data-ttu-id="471b7-103">Egy adatgyárban futtatott trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="471b7-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="471b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="471b7-104">SYNTAX</span></span>

### <span data-ttu-id="471b7-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="471b7-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="471b7-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471b7-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="471b7-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="471b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="471b7-108">DESCRIPTION</span></span>
<span data-ttu-id="471b7-109">A **stop-AzDataFactoryV2TriggerRun** parancsmag leállítja azt az indítót, amely az indító névvel és a trigger Run azonosítójával megadott adatgyárban fut.</span><span class="sxs-lookup"><span data-stu-id="471b7-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="471b7-110">Jelenleg csak az WaitingOnDependency-állapot TumblingWindowTriggers támogatott.</span><span class="sxs-lookup"><span data-stu-id="471b7-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="471b7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="471b7-111">EXAMPLES</span></span>

### <span data-ttu-id="471b7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="471b7-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="471b7-113">Ez a parancs a gyári WikiADF az "08586002468005888497807248799CU16" azonosítójú indítót futtatja.</span><span class="sxs-lookup"><span data-stu-id="471b7-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="471b7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="471b7-114">PARAMETERS</span></span>

### <span data-ttu-id="471b7-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="471b7-115">-DataFactory</span></span>
<span data-ttu-id="471b7-116">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="471b7-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="471b7-117">-DataFactoryName</span></span>
<span data-ttu-id="471b7-118">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="471b7-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471b7-119">-DefaultProfile</span></span>
<span data-ttu-id="471b7-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="471b7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="471b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="471b7-121">-InputObject</span></span>
<span data-ttu-id="471b7-122">Az indítással kapcsolatos információk.</span><span class="sxs-lookup"><span data-stu-id="471b7-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="471b7-123">-PassThru</span></span>
<span data-ttu-id="471b7-124">Ha meg van adva, akkor a parancsmag az igaz értéket adja meg, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="471b7-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="471b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="471b7-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="471b7-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="471b7-127">-TriggerName</span></span>
<span data-ttu-id="471b7-128">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="471b7-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="471b7-129">-TriggerRunId</span></span>
<span data-ttu-id="471b7-130">Az indító AZONOSÍTÓjának futtatása.</span><span class="sxs-lookup"><span data-stu-id="471b7-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471b7-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="471b7-131">-Confirm</span></span>
<span data-ttu-id="471b7-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="471b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="471b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="471b7-133">-WhatIf</span></span>
<span data-ttu-id="471b7-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="471b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="471b7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="471b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="471b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471b7-136">CommonParameters</span></span>
<span data-ttu-id="471b7-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="471b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471b7-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="471b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471b7-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="471b7-139">INPUTS</span></span>

### <span data-ttu-id="471b7-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="471b7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="471b7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="471b7-141">System.String</span></span>

### <span data-ttu-id="471b7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="471b7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="471b7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="471b7-143">OUTPUTS</span></span>

### <span data-ttu-id="471b7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="471b7-144">System.Boolean</span></span>

## <span data-ttu-id="471b7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="471b7-145">NOTES</span></span>

## <span data-ttu-id="471b7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="471b7-146">RELATED LINKS</span></span>
