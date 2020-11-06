---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: ef5b99a27c547ec1e71c2339de8f4c9536549981
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505103"
---
# <span data-ttu-id="8e8f5-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8e8f5-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="8e8f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8f5-103">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e8f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e8f5-104">SYNTAX</span></span>

### <span data-ttu-id="8e8f5-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e8f5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="8e8f5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8f5-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
```

### <span data-ttu-id="8e8f5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8e8f5-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="8e8f5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e8f5-108">DESCRIPTION</span></span>
<span data-ttu-id="8e8f5-109">Az Get-AzureRmDataFactoryV2IntegrationRuntime parancsmag adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="8e8f5-110">Ha az integrációs futtatókörnyezet nevét adja meg, ez a parancsmag információkat kap az integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="8e8f5-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="8e8f5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8e8f5-112">EXAMPLES</span></span>

### <span data-ttu-id="8e8f5-113">1. példa: az összes integrációs futtatókörnyezet listázása az adatgyárban</span><span class="sxs-lookup"><span data-stu-id="8e8f5-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="8e8f5-114">A ' teszt-DF-EU2 ' nevű adatfeldolgozóban található összes integrációs futtatókörnyezet felsorolása.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8e8f5-115">2. példa: felügyelt dedikált integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="8e8f5-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="8e8f5-116">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8e8f5-117">3. példa: a felügyelt dedikált integrációs futtatókörnyezet beszerzése részletes állapottal</span><span class="sxs-lookup"><span data-stu-id="8e8f5-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="8e8f5-118">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8e8f5-119">4. példa: önállóan működtetett integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="8e8f5-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="8e8f5-120">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="8e8f5-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e8f5-121">PARAMETERS</span></span>

### <span data-ttu-id="8e8f5-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e8f5-122">-DataFactoryName</span></span>
<span data-ttu-id="8e8f5-123">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8f5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8f5-124">-InputObject</span></span>
<span data-ttu-id="8e8f5-125">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-125">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8f5-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e8f5-126">-Name</span></span>
<span data-ttu-id="8e8f5-127">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-127">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e8f5-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8f5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8f5-130">-ResourceId</span></span>
<span data-ttu-id="8e8f5-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-131">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8f5-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="8e8f5-132">-Status</span></span>
<span data-ttu-id="8e8f5-133">Az integrációs futtatókörnyezet részletének állapota.</span><span class="sxs-lookup"><span data-stu-id="8e8f5-133">The integration runtime detail status.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8e8f5-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e8f5-134">INPUTS</span></span>

### <span data-ttu-id="8e8f5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8e8f5-135">System.String</span></span>
<span data-ttu-id="8e8f5-136">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8e8f5-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="8e8f5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e8f5-137">OUTPUTS</span></span>

### <span data-ttu-id="8e8f5-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8e8f5-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8e8f5-139">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntime Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8e8f5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>


## <span data-ttu-id="8e8f5-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e8f5-140">NOTES</span></span>
<span data-ttu-id="8e8f5-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="8e8f5-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8e8f5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e8f5-142">RELATED LINKS</span></span>
[<span data-ttu-id="8e8f5-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8e8f5-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="8e8f5-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8e8f5-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()