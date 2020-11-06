---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fd6e979b753bd5fea21af050492b194326122a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503804"
---
# <span data-ttu-id="2de4a-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de4a-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2de4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2de4a-102">SYNOPSIS</span></span>
<span data-ttu-id="2de4a-103">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="2de4a-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2de4a-104">SYNTAX</span></span>

### <span data-ttu-id="2de4a-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2de4a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de4a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2de4a-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de4a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2de4a-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de4a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2de4a-108">DESCRIPTION</span></span>
<span data-ttu-id="2de4a-109">Az Get-AzureRmDataFactoryV2IntegrationRuntime parancsmag adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="2de4a-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="2de4a-110">Ha az integrációs futtatókörnyezet nevét adja meg, ez a parancsmag információkat kap az integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="2de4a-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="2de4a-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="2de4a-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="2de4a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2de4a-112">EXAMPLES</span></span>

### <span data-ttu-id="2de4a-113">1. példa: az összes integrációs futtatókörnyezet listázása az adatgyárban</span><span class="sxs-lookup"><span data-stu-id="2de4a-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="2de4a-114">A ' teszt-DF-EU2 ' nevű adatfeldolgozóban található összes integrációs futtatókörnyezet felsorolása.</span><span class="sxs-lookup"><span data-stu-id="2de4a-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de4a-115">2. példa: felügyelt dedikált integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="2de4a-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="2de4a-116">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="2de4a-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de4a-117">3. példa: a felügyelt dedikált integrációs futtatókörnyezet beszerzése részletes állapottal</span><span class="sxs-lookup"><span data-stu-id="2de4a-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="2de4a-118">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="2de4a-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de4a-119">4. példa: önállóan működtetett integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="2de4a-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="2de4a-120">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="2de4a-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="2de4a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2de4a-121">PARAMETERS</span></span>

### <span data-ttu-id="2de4a-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2de4a-122">-DataFactoryName</span></span>
<span data-ttu-id="2de4a-123">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="2de4a-123">The data factory name.</span></span>

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

### <span data-ttu-id="2de4a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de4a-124">-DefaultProfile</span></span>
<span data-ttu-id="2de4a-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2de4a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de4a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2de4a-126">-InputObject</span></span>
<span data-ttu-id="2de4a-127">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="2de4a-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="2de4a-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2de4a-128">-Name</span></span>
<span data-ttu-id="2de4a-129">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="2de4a-129">The integration runtime name.</span></span>

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

### <span data-ttu-id="2de4a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de4a-130">-ResourceGroupName</span></span>
<span data-ttu-id="2de4a-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2de4a-131">The resource group name.</span></span>

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

### <span data-ttu-id="2de4a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2de4a-132">-ResourceId</span></span>
<span data-ttu-id="2de4a-133">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2de4a-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2de4a-134">-Állapot</span><span class="sxs-lookup"><span data-stu-id="2de4a-134">-Status</span></span>
<span data-ttu-id="2de4a-135">Az integrációs futtatókörnyezet részletének állapota.</span><span class="sxs-lookup"><span data-stu-id="2de4a-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="2de4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de4a-136">CommonParameters</span></span>
<span data-ttu-id="2de4a-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2de4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de4a-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de4a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de4a-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de4a-139">INPUTS</span></span>

### <span data-ttu-id="2de4a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2de4a-140">System.String</span></span>
<span data-ttu-id="2de4a-141">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de4a-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2de4a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de4a-142">OUTPUTS</span></span>

### <span data-ttu-id="2de4a-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2de4a-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2de4a-144">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntime Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de4a-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

## <span data-ttu-id="2de4a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2de4a-145">NOTES</span></span>
<span data-ttu-id="2de4a-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="2de4a-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2de4a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2de4a-147">RELATED LINKS</span></span>

[<span data-ttu-id="2de4a-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de4a-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="2de4a-149">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de4a-149">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()