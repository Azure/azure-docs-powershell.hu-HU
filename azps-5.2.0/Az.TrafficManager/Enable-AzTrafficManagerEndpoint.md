---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367161"
---
# <span data-ttu-id="44498-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="44498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44498-102">SYNOPSIS</span></span>
<span data-ttu-id="44498-103">Engedélyezi egy végpontot egy Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="44498-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="44498-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44498-104">SYNTAX</span></span>

### <span data-ttu-id="44498-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="44498-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44498-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="44498-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44498-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44498-107">DESCRIPTION</span></span>
<span data-ttu-id="44498-108">Az **Enable-AzTrafficManagerEndpoint** parancsmag egy Azure Traffic Manager-profilban engedélyezi a végpontokat.</span><span class="sxs-lookup"><span data-stu-id="44498-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="44498-109">A folyamat műveleti jelének használatával átadhat egy **TrafficManagerEndpoint-objektumot** ennek a parancsmagnak, vagy megadhat **egy TrafficManagerEndpoint-objektumot** a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="44498-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="44498-110">Másik lehetőségként megadhatja a végpont nevét és típusát a Name *and* *Type* paraméter használatával, a *ProfileName* és *az ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="44498-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="44498-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44498-111">EXAMPLES</span></span>

### <span data-ttu-id="44498-112">1. példa: Végpont engedélyezése profilból</span><span class="sxs-lookup"><span data-stu-id="44498-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="44498-113">Ez a parancs engedélyezi a contoso nevű külső végpontot a ContosoProfile nevű profilban az Erőforráscsoport11 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="44498-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="44498-114">2. példa: Végpont engedélyezése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="44498-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="44498-115">Ez a parancs a Contoso nevű külső végpontot az ResourceGroup11 ContosoProfile nevű profiljából kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44498-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="44498-116">A parancs ezután átadja a végpontot az **Enable-AzTrafficManagerEndpoint** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="44498-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44498-117">Ez a parancsmag engedélyezi ezt a végpontot.</span><span class="sxs-lookup"><span data-stu-id="44498-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="44498-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44498-118">PARAMETERS</span></span>

### <span data-ttu-id="44498-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44498-119">-DefaultProfile</span></span>
<span data-ttu-id="44498-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44498-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44498-121">-Name</span><span class="sxs-lookup"><span data-stu-id="44498-121">-Name</span></span>
<span data-ttu-id="44498-122">Megadja annak a Traffic Manager-végpontnak a nevét, amely ezt a parancsmagot engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="44498-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="44498-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="44498-123">-ProfileName</span></span>
<span data-ttu-id="44498-124">Annak a Traffic Manager-profilnak a nevét adja meg, amelyben ez a parancsmag egy végpontot tesz elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="44498-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="44498-125">Profil beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="44498-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="44498-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44498-126">-ResourceGroupName</span></span>
<span data-ttu-id="44498-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44498-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="44498-128">Ez a parancsmag engedélyezi a Traffic Manager-végpontot a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="44498-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="44498-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="44498-130">Ez a parancsmag által elérhető Traffic Manager-végpontot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="44498-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="44498-131">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="44498-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="44498-132">-Type</span><span class="sxs-lookup"><span data-stu-id="44498-132">-Type</span></span>
<span data-ttu-id="44498-133">Meghatározza, hogy a parancsmag milyen típusú végpontot tilt le a Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="44498-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="44498-134">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="44498-134">Valid values are:</span></span> 

- <span data-ttu-id="44498-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="44498-135">AzureEndpoints</span></span>
- <span data-ttu-id="44498-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="44498-136">ExternalEndpoints</span></span>
- <span data-ttu-id="44498-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="44498-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="44498-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44498-138">CommonParameters</span></span>
<span data-ttu-id="44498-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44498-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44498-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44498-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44498-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44498-141">INPUTS</span></span>

### <span data-ttu-id="44498-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="44498-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44498-143">OUTPUTS</span></span>

### <span data-ttu-id="44498-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44498-144">System.Boolean</span></span>

## <span data-ttu-id="44498-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44498-145">NOTES</span></span>

## <span data-ttu-id="44498-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44498-146">RELATED LINKS</span></span>

[<span data-ttu-id="44498-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="44498-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="44498-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="44498-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="44498-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="44498-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="44498-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="44498-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44498-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="44498-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="44498-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


