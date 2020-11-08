---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187377"
---
# <span data-ttu-id="f98f7-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f98f7-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="f98f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f98f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f98f7-103">Egy szolgáltatási példány törlése.</span><span class="sxs-lookup"><span data-stu-id="f98f7-103">Deletes a service instance.</span></span>

## <span data-ttu-id="f98f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f98f7-104">SYNTAX</span></span>

### <span data-ttu-id="f98f7-105">ServiceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f98f7-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98f7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98f7-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98f7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98f7-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f98f7-108">DESCRIPTION</span></span>
<span data-ttu-id="f98f7-109">Egy szolgáltatási példány törlése.</span><span class="sxs-lookup"><span data-stu-id="f98f7-109">Deletes a service instance.</span></span>

## <span data-ttu-id="f98f7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f98f7-110">EXAMPLES</span></span>

### <span data-ttu-id="f98f7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f98f7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="f98f7-112">A meglévő HealthcareApis-szolgáltatás törlése a megadott erőforráscsoporthoz tartozó névvel</span><span class="sxs-lookup"><span data-stu-id="f98f7-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="f98f7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f98f7-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="f98f7-114">A meglévő HealthcareApis-szolgáltatás törlése a megadott ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f98f7-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="f98f7-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="f98f7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="f98f7-116">A megadott HealthcareApis-szolgáltatási objektum törlése</span><span class="sxs-lookup"><span data-stu-id="f98f7-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="f98f7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f98f7-117">PARAMETERS</span></span>

### <span data-ttu-id="f98f7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f98f7-118">-AsJob</span></span>
<span data-ttu-id="f98f7-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f98f7-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f98f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98f7-120">-DefaultProfile</span></span>
<span data-ttu-id="f98f7-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f98f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98f7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f98f7-122">-InputObject</span></span>
<span data-ttu-id="f98f7-123">HealthcareApis szolgáltatás objektum</span><span class="sxs-lookup"><span data-stu-id="f98f7-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="f98f7-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f98f7-124">-Name</span></span>
<span data-ttu-id="f98f7-125">HealthcareApis szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f98f7-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="f98f7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f98f7-126">-PassThru</span></span>
<span data-ttu-id="f98f7-127">Ha a művelet sikeres, az igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f98f7-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="f98f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="f98f7-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f98f7-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f98f7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f98f7-130">-ResourceId</span></span>
<span data-ttu-id="f98f7-131">A HealthcareApis szolgáltatás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f98f7-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="f98f7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f98f7-132">-Confirm</span></span>
<span data-ttu-id="f98f7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f98f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98f7-134">-WhatIf</span></span>
<span data-ttu-id="f98f7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f98f7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98f7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f98f7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98f7-137">CommonParameters</span></span>
<span data-ttu-id="f98f7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f98f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98f7-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f98f7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98f7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f98f7-140">INPUTS</span></span>

### <span data-ttu-id="f98f7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f98f7-141">System.String</span></span>

### <span data-ttu-id="f98f7-142">Microsoft. Azure. Command. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f98f7-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="f98f7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f98f7-143">OUTPUTS</span></span>

### <span data-ttu-id="f98f7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f98f7-144">System.Boolean</span></span>

## <span data-ttu-id="f98f7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f98f7-145">NOTES</span></span>

## <span data-ttu-id="f98f7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f98f7-146">RELATED LINKS</span></span>