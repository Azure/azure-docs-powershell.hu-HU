---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847302"
---
# <span data-ttu-id="76433-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="76433-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76433-102">SYNOPSIS</span></span>
<span data-ttu-id="76433-103">Információt kap az integrációs futtatókörnyezet erőforrásairól.</span><span class="sxs-lookup"><span data-stu-id="76433-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="76433-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76433-104">SYNTAX</span></span>

### <span data-ttu-id="76433-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76433-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76433-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76433-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76433-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="76433-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76433-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76433-108">DESCRIPTION</span></span>
<span data-ttu-id="76433-109">Az Get-AzDataFactoryV2IntegrationRuntime parancsmag adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="76433-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="76433-110">Ha az integrációs futtatókörnyezet nevét adja meg, ez a parancsmag információkat kap az integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="76433-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="76433-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="76433-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="76433-112">Példák</span><span class="sxs-lookup"><span data-stu-id="76433-112">EXAMPLES</span></span>

### <span data-ttu-id="76433-113">1. példa: az összes integrációs futtatókörnyezet listázása az adatgyárban</span><span class="sxs-lookup"><span data-stu-id="76433-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="76433-114">A ' teszt-DF-EU2 ' nevű adatfeldolgozóban található összes integrációs futtatókörnyezet felsorolása.</span><span class="sxs-lookup"><span data-stu-id="76433-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="76433-115">2. példa: felügyelt dedikált integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="76433-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="76433-116">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="76433-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="76433-117">3. példa: a felügyelt dedikált integrációs futtatókörnyezet beszerzése részletes állapottal</span><span class="sxs-lookup"><span data-stu-id="76433-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="76433-118">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="76433-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="76433-119">4. példa: önállóan működtetett integrációs futtatókörnyezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="76433-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="76433-120">Ez a parancs információt jelenít meg az "RG-teszt-dfv2" nevű erőforráscsoport-előfizetéshez tartozó "teszt-dedikált-IR" nevű integrációs futtatókörnyezetről és a "teszt-DF-EU2" nevű adatfeldolgozóról.</span><span class="sxs-lookup"><span data-stu-id="76433-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="76433-121">Példa 5: önállóan működtetett integrációs futtatókörnyezet beszerzése részletes állapottal</span><span class="sxs-lookup"><span data-stu-id="76433-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="76433-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76433-122">PARAMETERS</span></span>

### <span data-ttu-id="76433-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="76433-123">-DataFactoryName</span></span>
<span data-ttu-id="76433-124">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="76433-124">The data factory name.</span></span>

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

### <span data-ttu-id="76433-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76433-125">-DefaultProfile</span></span>
<span data-ttu-id="76433-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76433-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76433-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76433-127">-InputObject</span></span>
<span data-ttu-id="76433-128">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="76433-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="76433-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76433-129">-Name</span></span>
<span data-ttu-id="76433-130">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="76433-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="76433-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76433-131">-ResourceGroupName</span></span>
<span data-ttu-id="76433-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="76433-132">The resource group name.</span></span>

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

### <span data-ttu-id="76433-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76433-133">-ResourceId</span></span>
<span data-ttu-id="76433-134">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="76433-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="76433-135">-Állapot</span><span class="sxs-lookup"><span data-stu-id="76433-135">-Status</span></span>
<span data-ttu-id="76433-136">Az integrációs futtatókörnyezet részletének állapota.</span><span class="sxs-lookup"><span data-stu-id="76433-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="76433-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76433-137">CommonParameters</span></span>
<span data-ttu-id="76433-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76433-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76433-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76433-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76433-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76433-140">INPUTS</span></span>

### <span data-ttu-id="76433-141">System. String</span><span class="sxs-lookup"><span data-stu-id="76433-141">System.String</span></span>

### <span data-ttu-id="76433-142">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="76433-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76433-143">OUTPUTS</span></span>

### <span data-ttu-id="76433-144">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="76433-145">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="76433-146">Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="76433-147">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="76433-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76433-148">NOTES</span></span>
<span data-ttu-id="76433-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="76433-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="76433-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76433-150">RELATED LINKS</span></span>

[<span data-ttu-id="76433-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="76433-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76433-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
