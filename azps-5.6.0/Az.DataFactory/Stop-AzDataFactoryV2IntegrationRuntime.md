---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942866"
---
# <span data-ttu-id="794ab-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="794ab-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="794ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="794ab-102">SYNOPSIS</span></span>
<span data-ttu-id="794ab-103">Leállítja a felügyelt dedikált integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="794ab-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="794ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="794ab-104">SYNTAX</span></span>

### <span data-ttu-id="794ab-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="794ab-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="794ab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="794ab-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794ab-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="794ab-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794ab-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="794ab-108">DESCRIPTION</span></span>
<span data-ttu-id="794ab-109">A **Stop-AzDataFactoryV2IntegrationRuntime** parancsmag leállítja a felügyelt dedikált integrációs futási futásiidőt "Elindítva" állapotban, amelyet a Start-AzDataFactoryV2IntegrationRuntime parancsmag indított el.</span><span class="sxs-lookup"><span data-stu-id="794ab-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="794ab-110">Az erőforrások felszabadulnak, az állam pedig a "Leállítva" állapotra átvitelt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="794ab-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="794ab-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="794ab-111">EXAMPLES</span></span>

### <span data-ttu-id="794ab-112">1. példa: "Elindítva" állapotban futó felügyelt integrációs futási idő leállítása.</span><span class="sxs-lookup"><span data-stu-id="794ab-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="794ab-113">A felügyelt integrációs futásidejű "test-reserlved-ir" "Elindítva" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="794ab-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="794ab-114">A Stop-AzDataFactoryV2IntegrationRuntime futtatása után az erőforrások felszabadulnak, az állam pedig "Leállítva" állapotba kerül.</span><span class="sxs-lookup"><span data-stu-id="794ab-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="794ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="794ab-115">PARAMETERS</span></span>

### <span data-ttu-id="794ab-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="794ab-116">-DataFactoryName</span></span>
<span data-ttu-id="794ab-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="794ab-117">The data factory name.</span></span>

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

### <span data-ttu-id="794ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794ab-118">-DefaultProfile</span></span>
<span data-ttu-id="794ab-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="794ab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="794ab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="794ab-120">-Force</span></span>
<span data-ttu-id="794ab-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="794ab-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="794ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="794ab-122">-InputObject</span></span>
<span data-ttu-id="794ab-123">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="794ab-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="794ab-124">-Name</span><span class="sxs-lookup"><span data-stu-id="794ab-124">-Name</span></span>
<span data-ttu-id="794ab-125">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="794ab-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="794ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="794ab-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="794ab-127">The resource group name.</span></span>

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

### <span data-ttu-id="794ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="794ab-128">-ResourceId</span></span>
<span data-ttu-id="794ab-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="794ab-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="794ab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="794ab-130">-Confirm</span></span>
<span data-ttu-id="794ab-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="794ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794ab-132">-WhatIf</span></span>
<span data-ttu-id="794ab-133">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="794ab-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="794ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794ab-134">CommonParameters</span></span>
<span data-ttu-id="794ab-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794ab-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="794ab-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794ab-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="794ab-137">INPUTS</span></span>

### <span data-ttu-id="794ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="794ab-138">System.String</span></span>

### <span data-ttu-id="794ab-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="794ab-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="794ab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="794ab-140">OUTPUTS</span></span>

### <span data-ttu-id="794ab-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="794ab-141">System.Void</span></span>

## <span data-ttu-id="794ab-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="794ab-142">NOTES</span></span>
<span data-ttu-id="794ab-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorok, másolás, tevékenységek, integráció futásideje</span><span class="sxs-lookup"><span data-stu-id="794ab-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="794ab-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="794ab-144">RELATED LINKS</span></span>

[<span data-ttu-id="794ab-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="794ab-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
