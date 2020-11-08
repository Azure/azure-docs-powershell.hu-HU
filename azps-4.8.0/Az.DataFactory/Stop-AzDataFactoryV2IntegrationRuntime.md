---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182836"
---
# <span data-ttu-id="ce719-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ce719-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ce719-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce719-102">SYNOPSIS</span></span>
<span data-ttu-id="ce719-103">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="ce719-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="ce719-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce719-104">SYNTAX</span></span>

### <span data-ttu-id="ce719-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce719-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce719-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce719-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce719-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ce719-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce719-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce719-108">DESCRIPTION</span></span>
<span data-ttu-id="ce719-109">A **stop-AzDataFactoryV2IntegrationRuntime** parancsmag a "Started" állapotú, felügyelt dedikált integrációs futtatókörnyezetet állítja le, amelyet az Start-AzDataFactoryV2IntegrationRuntime parancsmag kezdeményezett.</span><span class="sxs-lookup"><span data-stu-id="ce719-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="ce719-110">A program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="ce719-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="ce719-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ce719-111">EXAMPLES</span></span>

### <span data-ttu-id="ce719-112">1. példa: a felügyelt integrációs futtatókörnyezet leállítása "Started" állapotban.</span><span class="sxs-lookup"><span data-stu-id="ce719-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="ce719-113">A felügyelt integrációs futásidejű ' teszt-reserlved-IR ' "Started" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="ce719-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="ce719-114">Miután futtatta az Stop-AzDataFactoryV2IntegrationRuntime parancsmagot, a program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="ce719-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="ce719-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce719-115">PARAMETERS</span></span>

### <span data-ttu-id="ce719-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ce719-116">-DataFactoryName</span></span>
<span data-ttu-id="ce719-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ce719-117">The data factory name.</span></span>

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

### <span data-ttu-id="ce719-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce719-118">-DefaultProfile</span></span>
<span data-ttu-id="ce719-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce719-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce719-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ce719-120">-Force</span></span>
<span data-ttu-id="ce719-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ce719-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ce719-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce719-122">-InputObject</span></span>
<span data-ttu-id="ce719-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="ce719-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ce719-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce719-124">-Name</span></span>
<span data-ttu-id="ce719-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="ce719-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ce719-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce719-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce719-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce719-127">The resource group name.</span></span>

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

### <span data-ttu-id="ce719-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce719-128">-ResourceId</span></span>
<span data-ttu-id="ce719-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ce719-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ce719-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce719-130">-Confirm</span></span>
<span data-ttu-id="ce719-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce719-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce719-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce719-132">-WhatIf</span></span>
<span data-ttu-id="ce719-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ce719-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ce719-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce719-134">CommonParameters</span></span>
<span data-ttu-id="ce719-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce719-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce719-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce719-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce719-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce719-137">INPUTS</span></span>

### <span data-ttu-id="ce719-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ce719-138">System.String</span></span>

### <span data-ttu-id="ce719-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ce719-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ce719-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce719-140">OUTPUTS</span></span>

### <span data-ttu-id="ce719-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="ce719-141">System.Void</span></span>

## <span data-ttu-id="ce719-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce719-142">NOTES</span></span>
<span data-ttu-id="ce719-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="ce719-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ce719-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce719-144">RELATED LINKS</span></span>

[<span data-ttu-id="ce719-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ce719-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
