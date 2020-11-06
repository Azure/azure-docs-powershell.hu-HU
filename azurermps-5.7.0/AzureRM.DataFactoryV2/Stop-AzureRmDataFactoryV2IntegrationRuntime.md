---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ae319662cf7b839524bd44524d63a3ba0a15fe20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495418"
---
# <span data-ttu-id="5b7ec-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b7ec-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5b7ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7ec-103">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b7ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b7ec-104">SYNTAX</span></span>

### <span data-ttu-id="5b7ec-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b7ec-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b7ec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7ec-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7ec-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5b7ec-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b7ec-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7ec-109">A **stop-AzureRmDataFactoryV2IntegrationRuntime** parancsmag a "Started" állapotú, felügyelt dedikált integrációs futtatókörnyezetet állítja le, amelyet az Start-AzureRmDataFactoryV2IntegrationRuntime parancsmag kezdeményezett.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="5b7ec-110">A program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5b7ec-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5b7ec-111">EXAMPLES</span></span>

### <span data-ttu-id="5b7ec-112">1. példa: a felügyelt integrációs futtatókörnyezet leállítása "Started" állapotban.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="5b7ec-113">A felügyelt integrációs futásidejű ' teszt-reserlved-IR ' "Started" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="5b7ec-114">Miután futtatta az Stop-AzureRmDataFactoryV2IntegrationRuntime parancsmagot, a program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5b7ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-115">PARAMETERS</span></span>

### <span data-ttu-id="5b7ec-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5b7ec-116">-DataFactoryName</span></span>
<span data-ttu-id="5b7ec-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-117">The data factory name.</span></span>

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

### <span data-ttu-id="5b7ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7ec-118">-DefaultProfile</span></span>
<span data-ttu-id="5b7ec-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b7ec-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5b7ec-120">-Force</span></span>
<span data-ttu-id="5b7ec-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b7ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b7ec-122">-InputObject</span></span>
<span data-ttu-id="5b7ec-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="5b7ec-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b7ec-124">-Name</span></span>
<span data-ttu-id="5b7ec-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-125">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b7ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b7ec-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-127">The resource group name.</span></span>

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

### <span data-ttu-id="5b7ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7ec-128">-ResourceId</span></span>
<span data-ttu-id="5b7ec-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b7ec-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b7ec-130">-Confirm</span></span>
<span data-ttu-id="5b7ec-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b7ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7ec-132">-WhatIf</span></span>
<span data-ttu-id="5b7ec-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b7ec-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b7ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7ec-134">CommonParameters</span></span>
<span data-ttu-id="5b7ec-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b7ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7ec-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7ec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7ec-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-137">INPUTS</span></span>

### <span data-ttu-id="5b7ec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5b7ec-138">System.String</span></span>
<span data-ttu-id="5b7ec-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b7ec-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5b7ec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-140">OUTPUTS</span></span>

### <span data-ttu-id="5b7ec-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b7ec-141">System.Boolean</span></span>

## <span data-ttu-id="5b7ec-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b7ec-142">NOTES</span></span>
<span data-ttu-id="5b7ec-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="5b7ec-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5b7ec-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b7ec-144">RELATED LINKS</span></span>

[<span data-ttu-id="5b7ec-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b7ec-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
