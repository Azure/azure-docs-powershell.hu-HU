---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 448b400d4a01924d7ef2ce64acc0f7edf827b827
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013173"
---
# <span data-ttu-id="69ede-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="69ede-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="69ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ede-102">SYNOPSIS</span></span>
<span data-ttu-id="69ede-103">Szolgáltatáspéldány törlése.</span><span class="sxs-lookup"><span data-stu-id="69ede-103">Deletes a service instance.</span></span>

## <span data-ttu-id="69ede-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69ede-104">SYNTAX</span></span>

### <span data-ttu-id="69ede-105">ServiceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69ede-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ede-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ede-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ede-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ede-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ede-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69ede-108">DESCRIPTION</span></span>
<span data-ttu-id="69ede-109">Szolgáltatáspéldány törlése.</span><span class="sxs-lookup"><span data-stu-id="69ede-109">Deletes a service instance.</span></span>

## <span data-ttu-id="69ede-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69ede-110">EXAMPLES</span></span>

### <span data-ttu-id="69ede-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="69ede-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="69ede-112">Törli a meglévő HealthcareApis szolgáltatást a megadott névvel egy megadott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="69ede-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="69ede-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="69ede-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="69ede-114">Törli a meglévő HealthcareApis szolgáltatást a megadott ResourceId-val.</span><span class="sxs-lookup"><span data-stu-id="69ede-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="69ede-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="69ede-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="69ede-116">Törli a megadott HealthcareApis szolgáltatásobjektumot.</span><span class="sxs-lookup"><span data-stu-id="69ede-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="69ede-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69ede-117">PARAMETERS</span></span>

### <span data-ttu-id="69ede-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ede-118">-AsJob</span></span>
<span data-ttu-id="69ede-119">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="69ede-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="69ede-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ede-120">-DefaultProfile</span></span>
<span data-ttu-id="69ede-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69ede-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ede-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69ede-122">-InputObject</span></span>
<span data-ttu-id="69ede-123">HealthcareApis service object</span><span class="sxs-lookup"><span data-stu-id="69ede-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ede-124">-Name</span><span class="sxs-lookup"><span data-stu-id="69ede-124">-Name</span></span>
<span data-ttu-id="69ede-125">HealthcareApis szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="69ede-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ede-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ede-126">-PassThru</span></span>
<span data-ttu-id="69ede-127">Ha meg van biztosítanak, a függvény eredménye igaz, ha a művelet sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="69ede-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="69ede-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ede-128">-ResourceGroupName</span></span>
<span data-ttu-id="69ede-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69ede-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ede-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ede-130">-ResourceId</span></span>
<span data-ttu-id="69ede-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="69ede-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ede-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69ede-132">-Confirm</span></span>
<span data-ttu-id="69ede-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="69ede-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ede-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ede-134">-WhatIf</span></span>
<span data-ttu-id="69ede-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="69ede-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ede-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69ede-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ede-137">CommonParameters</span></span>
<span data-ttu-id="69ede-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ede-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69ede-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ede-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69ede-140">INPUTS</span></span>

### <span data-ttu-id="69ede-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="69ede-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="69ede-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69ede-142">System.String</span></span>

## <span data-ttu-id="69ede-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ede-143">OUTPUTS</span></span>

### <span data-ttu-id="69ede-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69ede-144">System.Boolean</span></span>

## <span data-ttu-id="69ede-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69ede-145">NOTES</span></span>

## <span data-ttu-id="69ede-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69ede-146">RELATED LINKS</span></span>
