---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: c0932dcefe6d833e64c83eb8b034b812e7bf3430
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666960"
---
# <span data-ttu-id="78c5c-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="78c5c-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="78c5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="78c5c-103">Felügyelt dedikált integrációs futtatókörnyezetet indít el.</span><span class="sxs-lookup"><span data-stu-id="78c5c-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="78c5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78c5c-104">SYNTAX</span></span>

### <span data-ttu-id="78c5c-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78c5c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78c5c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78c5c-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c5c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="78c5c-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="78c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="78c5c-109">A **Start-AzDataFactoryV2IntegrationRuntime** parancsmag a felügyelt dedikált integrációs futtatókörnyezetet indítja el.</span><span class="sxs-lookup"><span data-stu-id="78c5c-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="78c5c-110">Az erőforrás kiépítve, és azt követően, hogy a művelet az "Elindítva" állapotú.</span><span class="sxs-lookup"><span data-stu-id="78c5c-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="78c5c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="78c5c-111">EXAMPLES</span></span>

### <span data-ttu-id="78c5c-112">1. példa: integrációs futtatókörnyezet indítása</span><span class="sxs-lookup"><span data-stu-id="78c5c-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="78c5c-113">Ez a parancsmag a "teszt-dedikált-IR" nevű felügyelt dedikált integrációs futtatókörnyezetet indítja el.</span><span class="sxs-lookup"><span data-stu-id="78c5c-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="78c5c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78c5c-114">PARAMETERS</span></span>

### <span data-ttu-id="78c5c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78c5c-115">-DataFactoryName</span></span>
<span data-ttu-id="78c5c-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="78c5c-116">The data factory name.</span></span>

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

### <span data-ttu-id="78c5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c5c-117">-DefaultProfile</span></span>
<span data-ttu-id="78c5c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78c5c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78c5c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78c5c-119">-Force</span></span>
<span data-ttu-id="78c5c-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="78c5c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="78c5c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78c5c-121">-InputObject</span></span>
<span data-ttu-id="78c5c-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="78c5c-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="78c5c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78c5c-123">-Name</span></span>
<span data-ttu-id="78c5c-124">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="78c5c-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c5c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c5c-125">-ResourceGroupName</span></span>
<span data-ttu-id="78c5c-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="78c5c-126">The resource group name.</span></span>

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

### <span data-ttu-id="78c5c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78c5c-127">-ResourceId</span></span>
<span data-ttu-id="78c5c-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="78c5c-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="78c5c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78c5c-129">-Confirm</span></span>
<span data-ttu-id="78c5c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78c5c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c5c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c5c-131">-WhatIf</span></span>
<span data-ttu-id="78c5c-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="78c5c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="78c5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c5c-133">CommonParameters</span></span>
<span data-ttu-id="78c5c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78c5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c5c-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c5c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c5c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78c5c-136">INPUTS</span></span>

### <span data-ttu-id="78c5c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="78c5c-137">System.String</span></span>

### <span data-ttu-id="78c5c-138">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="78c5c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="78c5c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78c5c-139">OUTPUTS</span></span>

### <span data-ttu-id="78c5c-140">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="78c5c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="78c5c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78c5c-141">NOTES</span></span>

## <span data-ttu-id="78c5c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78c5c-142">RELATED LINKS</span></span>

[<span data-ttu-id="78c5c-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="78c5c-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
