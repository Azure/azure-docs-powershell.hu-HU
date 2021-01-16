---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366951"
---
# <span data-ttu-id="58eb1-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="58eb1-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="58eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="58eb1-103">Frissíti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="58eb1-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="58eb1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58eb1-104">SYNTAX</span></span>

### <span data-ttu-id="58eb1-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58eb1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58eb1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58eb1-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58eb1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="58eb1-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58eb1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58eb1-108">DESCRIPTION</span></span>
<span data-ttu-id="58eb1-109">Az **Update-AzDataFactoryV2IntegrationRuntimeNode** parancsmag frissíti az önkiszolgáló integrációs futásidejű csomópont tulajdonságait egy adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="58eb1-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="58eb1-110">Jelenleg csak az "ConcurrentJobsLimit" frissítését támogatja.</span><span class="sxs-lookup"><span data-stu-id="58eb1-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="58eb1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58eb1-111">EXAMPLES</span></span>

### <span data-ttu-id="58eb1-112">1. példa: Az önkiszolgáló integráció futásidejű csomópontjának frissítése</span><span class="sxs-lookup"><span data-stu-id="58eb1-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="58eb1-113">A parancsmag frissíti a "ConcurrentCmsLimit" 3-asra a "Node_1" csomópontot az önkiszolgáló integrációs futásidejű "test-selfhost-ir" környezetben.</span><span class="sxs-lookup"><span data-stu-id="58eb1-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="58eb1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58eb1-114">PARAMETERS</span></span>

### <span data-ttu-id="58eb1-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="58eb1-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="58eb1-116">Az integrációs futásidejű csomóponton futtatható párhuzamos feladatok száma.</span><span class="sxs-lookup"><span data-stu-id="58eb1-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="58eb1-117">Az 1 és a maxConcurrentÚts közötti értékek megengedettek.</span><span class="sxs-lookup"><span data-stu-id="58eb1-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="58eb1-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58eb1-118">-DataFactoryName</span></span>
<span data-ttu-id="58eb1-119">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="58eb1-119">The data factory name.</span></span>

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

### <span data-ttu-id="58eb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58eb1-120">-DefaultProfile</span></span>
<span data-ttu-id="58eb1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58eb1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58eb1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58eb1-122">-InputObject</span></span>
<span data-ttu-id="58eb1-123">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="58eb1-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="58eb1-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="58eb1-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="58eb1-125">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="58eb1-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="58eb1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="58eb1-126">-Name</span></span>
<span data-ttu-id="58eb1-127">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="58eb1-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="58eb1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58eb1-128">-ResourceGroupName</span></span>
<span data-ttu-id="58eb1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58eb1-129">The resource group name.</span></span>

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

### <span data-ttu-id="58eb1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58eb1-130">-ResourceId</span></span>
<span data-ttu-id="58eb1-131">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="58eb1-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="58eb1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58eb1-132">-Confirm</span></span>
<span data-ttu-id="58eb1-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58eb1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58eb1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58eb1-134">-WhatIf</span></span>
<span data-ttu-id="58eb1-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58eb1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58eb1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58eb1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58eb1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58eb1-137">CommonParameters</span></span>
<span data-ttu-id="58eb1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58eb1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58eb1-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58eb1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58eb1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58eb1-140">INPUTS</span></span>

### <span data-ttu-id="58eb1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="58eb1-141">System.String</span></span>

### <span data-ttu-id="58eb1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58eb1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="58eb1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58eb1-143">OUTPUTS</span></span>

### <span data-ttu-id="58eb1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="58eb1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="58eb1-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58eb1-145">NOTES</span></span>
<span data-ttu-id="58eb1-146">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorok, másolás, tevékenységek, integráció futásideje</span><span class="sxs-lookup"><span data-stu-id="58eb1-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="58eb1-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58eb1-147">RELATED LINKS</span></span>

<span data-ttu-id="58eb1-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="58eb1-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

