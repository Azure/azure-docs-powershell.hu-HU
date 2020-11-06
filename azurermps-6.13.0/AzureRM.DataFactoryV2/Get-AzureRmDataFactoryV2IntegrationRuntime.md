---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 83e6de07f7796e49732a35cfea4573002e6208df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499632"
---
# <span data-ttu-id="c96b3-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c96b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c96b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c96b3-103">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="c96b3-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c96b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c96b3-104">SYNTAX</span></span>

### <span data-ttu-id="c96b3-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c96b3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96b3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c96b3-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96b3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c96b3-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96b3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c96b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c96b3-109">Az Get-AzureRmDataFactoryV2IntegrationRuntime parancsmag adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="c96b3-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="c96b3-110">Ha az integrációs futtatókörnyezet nevét adja meg, ez a parancsmag információkat kap az integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="c96b3-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="c96b3-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="c96b3-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="c96b3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c96b3-112">EXAMPLES</span></span>

### <span data-ttu-id="c96b3-113">1. példa: az összes integrációs futtatókörnyezet listázása az adatgyárban</span><span class="sxs-lookup"><span data-stu-id="c96b3-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="c96b3-114">A ' teszt-DF-EU2 ' nevű adatfeldolgozóban található összes integrációs futtatókörnyezet felsorolása.</span><span class="sxs-lookup"><span data-stu-id="c96b3-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="c96b3-115">2. példa: felügyelt dedikált integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="c96b3-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="c96b3-116">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="c96b3-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="c96b3-117">3. példa: a felügyelt dedikált integrációs futtatókörnyezet beszerzése részletes állapottal</span><span class="sxs-lookup"><span data-stu-id="c96b3-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="c96b3-118">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="c96b3-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="c96b3-119">4. példa: önállóan működtetett integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="c96b3-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="c96b3-120">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="c96b3-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="c96b3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c96b3-121">PARAMETERS</span></span>

### <span data-ttu-id="c96b3-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c96b3-122">-DataFactoryName</span></span>
<span data-ttu-id="c96b3-123">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c96b3-123">The data factory name.</span></span>

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

### <span data-ttu-id="c96b3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96b3-124">-DefaultProfile</span></span>
<span data-ttu-id="c96b3-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c96b3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96b3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c96b3-126">-InputObject</span></span>
<span data-ttu-id="c96b3-127">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="c96b3-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="c96b3-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c96b3-128">-Name</span></span>
<span data-ttu-id="c96b3-129">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="c96b3-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96b3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96b3-130">-ResourceGroupName</span></span>
<span data-ttu-id="c96b3-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c96b3-131">The resource group name.</span></span>

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

### <span data-ttu-id="c96b3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c96b3-132">-ResourceId</span></span>
<span data-ttu-id="c96b3-133">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c96b3-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c96b3-134">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c96b3-134">-Status</span></span>
<span data-ttu-id="c96b3-135">Az integrációs futtatókörnyezet részletének állapota.</span><span class="sxs-lookup"><span data-stu-id="c96b3-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="c96b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96b3-136">CommonParameters</span></span>
<span data-ttu-id="c96b3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c96b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96b3-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96b3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96b3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c96b3-139">INPUTS</span></span>

### <span data-ttu-id="c96b3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c96b3-140">System.String</span></span>

### <span data-ttu-id="c96b3-141">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="c96b3-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c96b3-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c96b3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c96b3-143">OUTPUTS</span></span>

### <span data-ttu-id="c96b3-144">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="c96b3-145">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="c96b3-146">Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="c96b3-147">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="c96b3-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c96b3-148">NOTES</span></span>
<span data-ttu-id="c96b3-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="c96b3-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c96b3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c96b3-150">RELATED LINKS</span></span>

[<span data-ttu-id="c96b3-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="c96b3-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c96b3-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
