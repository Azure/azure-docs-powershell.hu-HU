---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce9ca0f1581bc995f9ea18b3b87169ed979dd92c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502967"
---
# <span data-ttu-id="28af8-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="28af8-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="28af8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28af8-102">SYNOPSIS</span></span>
<span data-ttu-id="28af8-103">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="28af8-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28af8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28af8-104">SYNTAX</span></span>

### <span data-ttu-id="28af8-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28af8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28af8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="28af8-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28af8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="28af8-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28af8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="28af8-108">DESCRIPTION</span></span>
<span data-ttu-id="28af8-109">A **stop-AzureRmDataFactoryV2IntegrationRuntime** parancsmag a "Started" állapotú, felügyelt dedikált integrációs futtatókörnyezetet állítja le, amelyet az Start-AzureRmDataFactoryV2IntegrationRuntime parancsmag kezdeményezett.</span><span class="sxs-lookup"><span data-stu-id="28af8-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="28af8-110">A program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="28af8-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="28af8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="28af8-111">EXAMPLES</span></span>

### <span data-ttu-id="28af8-112">1. példa: a felügyelt integrációs futtatókörnyezet leállítása "Started" állapotban.</span><span class="sxs-lookup"><span data-stu-id="28af8-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="28af8-113">A felügyelt integrációs futásidejű ' teszt-reserlved-IR ' "Started" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="28af8-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="28af8-114">Miután futtatta az Stop-AzureRmDataFactoryV2IntegrationRuntime parancsmagot, a program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="28af8-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="28af8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28af8-115">PARAMETERS</span></span>

### <span data-ttu-id="28af8-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="28af8-116">-DataFactoryName</span></span>
<span data-ttu-id="28af8-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="28af8-117">The data factory name.</span></span>

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

### <span data-ttu-id="28af8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28af8-118">-DefaultProfile</span></span>
<span data-ttu-id="28af8-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28af8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28af8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="28af8-120">-Force</span></span>
<span data-ttu-id="28af8-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="28af8-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="28af8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28af8-122">-InputObject</span></span>
<span data-ttu-id="28af8-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="28af8-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="28af8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28af8-124">-Name</span></span>
<span data-ttu-id="28af8-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="28af8-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="28af8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28af8-126">-ResourceGroupName</span></span>
<span data-ttu-id="28af8-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="28af8-127">The resource group name.</span></span>

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

### <span data-ttu-id="28af8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28af8-128">-ResourceId</span></span>
<span data-ttu-id="28af8-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="28af8-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="28af8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28af8-130">-Confirm</span></span>
<span data-ttu-id="28af8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28af8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28af8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28af8-132">-WhatIf</span></span>
<span data-ttu-id="28af8-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28af8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="28af8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28af8-134">CommonParameters</span></span>
<span data-ttu-id="28af8-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28af8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28af8-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28af8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28af8-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28af8-137">INPUTS</span></span>

### <span data-ttu-id="28af8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="28af8-138">System.String</span></span>

### <span data-ttu-id="28af8-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="28af8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="28af8-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28af8-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="28af8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28af8-141">OUTPUTS</span></span>

### <span data-ttu-id="28af8-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="28af8-142">System.Void</span></span>

## <span data-ttu-id="28af8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28af8-143">NOTES</span></span>
<span data-ttu-id="28af8-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="28af8-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="28af8-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28af8-145">RELATED LINKS</span></span>

[<span data-ttu-id="28af8-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="28af8-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
