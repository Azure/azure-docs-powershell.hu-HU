---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149811"
---
# <span data-ttu-id="062ba-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="062ba-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="062ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="062ba-102">SYNOPSIS</span></span>
<span data-ttu-id="062ba-103">Eltávolít egy végpontot a Traffic Managerből.</span><span class="sxs-lookup"><span data-stu-id="062ba-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="062ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="062ba-104">SYNTAX</span></span>

### <span data-ttu-id="062ba-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="062ba-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="062ba-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="062ba-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="062ba-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="062ba-107">DESCRIPTION</span></span>
<span data-ttu-id="062ba-108">A **Remove-AzTrafficManagerEndpoint** parancsmag eltávolít egy végpontot az Azure Traffic Managerből.</span><span class="sxs-lookup"><span data-stu-id="062ba-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="062ba-109">Ez a parancsmag minden változtatást véglegesen a Traffic Manager szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="062ba-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="062ba-110">Ha több végpontot szeretne eltávolítani egy helyi Traffic Manager-profilobjektumból, és egyetlen művelettel szeretné véglegesni a módosításokat, használja a Remove-AzTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="062ba-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="062ba-111">A folyamat műveleti jelének használatával átadhat egy **TrafficManagerEndpoint-objektumot** ennek a parancsmagnak, vagy megadhat **egy TrafficManagerEndpoint-objektumot** a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="062ba-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="062ba-112">Másik lehetőségként megadhatja a végpont nevét és típusát a Name *and* *Type* paraméter használatával, a *ProfileName* és *az ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="062ba-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="062ba-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="062ba-113">EXAMPLES</span></span>

### <span data-ttu-id="062ba-114">1. példa: Végpont eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="062ba-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="062ba-115">Ez a parancs eltávolítja a contoso nevű Azure-végpontot az Erőforráscsoport11 nevű erőforráscsoport ContosoProfile nevű profiljából.</span><span class="sxs-lookup"><span data-stu-id="062ba-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="062ba-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="062ba-116">PARAMETERS</span></span>

### <span data-ttu-id="062ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062ba-117">-DefaultProfile</span></span>
<span data-ttu-id="062ba-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="062ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="062ba-119">-Force</span><span class="sxs-lookup"><span data-stu-id="062ba-119">-Force</span></span>
<span data-ttu-id="062ba-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="062ba-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="062ba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="062ba-121">-Name</span></span>
<span data-ttu-id="062ba-122">Annak a Traffic Manager-végpontnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="062ba-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="062ba-123">-ProfileName</span></span>
<span data-ttu-id="062ba-124">Annak a Traffic Manager-profilnak a nevét adja meg, amelyből a parancsmag eltávolít egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="062ba-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="062ba-125">Profil beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="062ba-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="062ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="062ba-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="062ba-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="062ba-128">Ez a parancsmag eltávolít egy Traffic Manager-végpontot a Paraméter által megadott csoport Forgalomkezelő-profiljából.</span><span class="sxs-lookup"><span data-stu-id="062ba-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="062ba-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="062ba-130">Azt a Traffic Manager-végpontot adja meg, amelyről ez a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="062ba-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="062ba-131">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="062ba-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-132">-Type</span><span class="sxs-lookup"><span data-stu-id="062ba-132">-Type</span></span>
<span data-ttu-id="062ba-133">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="062ba-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="062ba-134">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="062ba-134">Valid values are:</span></span> 

- <span data-ttu-id="062ba-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="062ba-135">AzureEndpoints</span></span>
- <span data-ttu-id="062ba-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="062ba-136">ExternalEndpoints</span></span>
- <span data-ttu-id="062ba-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="062ba-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="062ba-138">-Confirm</span></span>
<span data-ttu-id="062ba-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="062ba-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="062ba-140">-WhatIf</span></span>
<span data-ttu-id="062ba-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="062ba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="062ba-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="062ba-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="062ba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062ba-143">CommonParameters</span></span>
<span data-ttu-id="062ba-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062ba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062ba-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="062ba-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062ba-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="062ba-146">INPUTS</span></span>

### <span data-ttu-id="062ba-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="062ba-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="062ba-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="062ba-148">OUTPUTS</span></span>

### <span data-ttu-id="062ba-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="062ba-149">System.Boolean</span></span>

## <span data-ttu-id="062ba-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="062ba-150">NOTES</span></span>

## <span data-ttu-id="062ba-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="062ba-151">RELATED LINKS</span></span>

[<span data-ttu-id="062ba-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="062ba-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="062ba-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="062ba-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="062ba-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="062ba-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="062ba-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="062ba-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="062ba-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="062ba-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


