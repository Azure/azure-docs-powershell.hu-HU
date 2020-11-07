---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 67ce6dab34f907babd11bf180b499d25cfe9a053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666940"
---
# <span data-ttu-id="8d094-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8d094-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="8d094-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d094-102">SYNOPSIS</span></span>
<span data-ttu-id="8d094-103">Frissítheti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="8d094-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="8d094-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d094-104">SYNTAX</span></span>

### <span data-ttu-id="8d094-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d094-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d094-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d094-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d094-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8d094-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d094-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d094-108">DESCRIPTION</span></span>
<span data-ttu-id="8d094-109">Az **Update-AzDataFactoryV2IntegrationRuntimeNode** parancsmag frissíti az önálló, integrációs futtatókörnyezetek tulajdonságait az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="8d094-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="8d094-110">Jelenleg csak az "ConcurrentJobsLimit" frissítését támogatja.</span><span class="sxs-lookup"><span data-stu-id="8d094-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="8d094-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8d094-111">EXAMPLES</span></span>

### <span data-ttu-id="8d094-112">1. példa: az önálló integrációs futásidejű csomópont frissítése</span><span class="sxs-lookup"><span data-stu-id="8d094-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="8d094-113">A parancsmag a "ConcurrentJobsLimit" Node_1 és a "selfhost-IR"-es "</span><span class="sxs-lookup"><span data-stu-id="8d094-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8d094-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d094-114">PARAMETERS</span></span>

### <span data-ttu-id="8d094-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="8d094-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="8d094-116">Az egyidejű munkafolyamatok száma az integrációs futtatókörnyezet-csomóponton.</span><span class="sxs-lookup"><span data-stu-id="8d094-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="8d094-117">Az 1 és a maxConcurrentJobs közötti értékek engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="8d094-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8d094-118">-DataFactoryName</span></span>
<span data-ttu-id="8d094-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8d094-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d094-120">-DefaultProfile</span></span>
<span data-ttu-id="8d094-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d094-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d094-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d094-122">-InputObject</span></span>
<span data-ttu-id="8d094-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="8d094-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8d094-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8d094-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="8d094-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d094-126">-Name</span></span>
<span data-ttu-id="8d094-127">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="8d094-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="8d094-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d094-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d094-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d094-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d094-130">-ResourceId</span></span>
<span data-ttu-id="8d094-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8d094-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d094-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d094-132">-Confirm</span></span>
<span data-ttu-id="8d094-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d094-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d094-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d094-134">-WhatIf</span></span>
<span data-ttu-id="8d094-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d094-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d094-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d094-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d094-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d094-137">CommonParameters</span></span>
<span data-ttu-id="8d094-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d094-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d094-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d094-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d094-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d094-140">INPUTS</span></span>

### <span data-ttu-id="8d094-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8d094-141">System.String</span></span>

### <span data-ttu-id="8d094-142">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8d094-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8d094-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d094-143">OUTPUTS</span></span>

### <span data-ttu-id="8d094-144">Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8d094-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="8d094-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d094-145">NOTES</span></span>
<span data-ttu-id="8d094-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="8d094-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8d094-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d094-147">RELATED LINKS</span></span>

<span data-ttu-id="8d094-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="8d094-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

