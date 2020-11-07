---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846738"
---
# <span data-ttu-id="e44fa-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fa-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e44fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e44fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e44fa-103">Végpont eltávolítása a Traffic Managerből.</span><span class="sxs-lookup"><span data-stu-id="e44fa-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="e44fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e44fa-104">SYNTAX</span></span>

### <span data-ttu-id="e44fa-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="e44fa-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e44fa-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="e44fa-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e44fa-107">DESCRIPTION</span></span>
<span data-ttu-id="e44fa-108">A **Remove-AzTrafficManagerEndpoint** parancsmag eltávolítja az Azure Traffic Manager végpontját.</span><span class="sxs-lookup"><span data-stu-id="e44fa-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="e44fa-109">Ez a parancsmag minden módosítást véglegesít a Traffic Manager szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e44fa-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="e44fa-110">Ha több végpontot szeretne eltávolítani egy helyi forgalomirányítási profil-objektumból, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Remove-AzTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e44fa-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="e44fa-111">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy megadhat egy **TrafficManagerEndpoint** -objektumot a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="e44fa-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="e44fa-112">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="e44fa-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="e44fa-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e44fa-113">EXAMPLES</span></span>

### <span data-ttu-id="e44fa-114">Példa 1: végpont eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="e44fa-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="e44fa-115">Ez a parancs eltávolítja a contoso nevű Azure-végpontot az ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljából.</span><span class="sxs-lookup"><span data-stu-id="e44fa-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e44fa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e44fa-116">PARAMETERS</span></span>

### <span data-ttu-id="e44fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44fa-117">-DefaultProfile</span></span>
<span data-ttu-id="e44fa-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e44fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44fa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e44fa-119">-Force</span></span>
<span data-ttu-id="e44fa-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e44fa-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e44fa-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e44fa-121">-Name</span></span>
<span data-ttu-id="e44fa-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e44fa-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e44fa-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e44fa-123">-ProfileName</span></span>
<span data-ttu-id="e44fa-124">Annak a forgalomirányító-profilnak a neve, amelyből a parancsmag eltávolítja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="e44fa-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="e44fa-125">Ha profilt szeretne beolvasni, használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e44fa-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="e44fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="e44fa-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e44fa-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e44fa-128">Ez a parancsmag a forgalomirányító végpontját eltávolítja a forgalomirányító-profilból abban a csoportban, amelyben ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="e44fa-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e44fa-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fa-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e44fa-130">A forgalomirányító végpontját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="e44fa-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="e44fa-131">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e44fa-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e44fa-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e44fa-132">-Type</span></span>
<span data-ttu-id="e44fa-133">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="e44fa-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="e44fa-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e44fa-134">Valid values are:</span></span> 

- <span data-ttu-id="e44fa-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="e44fa-135">AzureEndpoints</span></span>
- <span data-ttu-id="e44fa-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="e44fa-136">ExternalEndpoints</span></span>
- <span data-ttu-id="e44fa-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="e44fa-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="e44fa-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e44fa-138">-Confirm</span></span>
<span data-ttu-id="e44fa-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e44fa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44fa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44fa-140">-WhatIf</span></span>
<span data-ttu-id="e44fa-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e44fa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44fa-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e44fa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44fa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44fa-143">CommonParameters</span></span>
<span data-ttu-id="e44fa-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e44fa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44fa-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44fa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44fa-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e44fa-146">INPUTS</span></span>

### <span data-ttu-id="e44fa-147">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fa-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e44fa-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e44fa-148">OUTPUTS</span></span>

### <span data-ttu-id="e44fa-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e44fa-149">System.Boolean</span></span>

## <span data-ttu-id="e44fa-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e44fa-150">NOTES</span></span>

## <span data-ttu-id="e44fa-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e44fa-151">RELATED LINKS</span></span>

[<span data-ttu-id="e44fa-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fa-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e44fa-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e44fa-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e44fa-154">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e44fa-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e44fa-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e44fa-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e44fa-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e44fa-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


