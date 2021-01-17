---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338837"
---
# <span data-ttu-id="5bcff-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5bcff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bcff-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcff-103">Letilt egy végpontot egy Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="5bcff-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="5bcff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bcff-104">SYNTAX</span></span>

### <span data-ttu-id="5bcff-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="5bcff-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcff-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="5bcff-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bcff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bcff-107">DESCRIPTION</span></span>
<span data-ttu-id="5bcff-108">A **Disable-AzTrafficManagerEndpoint** parancsmag letilt egy végpontot egy Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="5bcff-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="5bcff-109">A folyamat műveleti jelének használatával átadhat egy **TrafficManagerEndpoint-objektumot** ennek a parancsmagnak, vagy a **TrafficManagerEndpoint-objektumot** a *TrafficManagerEndpoint* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="5bcff-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="5bcff-110">Másik lehetőségként megadhatja a végpont nevét és típusát a Name *and* *Type* paraméter használatával, a *ProfileName* és *az ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="5bcff-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="5bcff-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bcff-111">EXAMPLES</span></span>

### <span data-ttu-id="5bcff-112">1. példa: Egy végpont letiltása név szerint</span><span class="sxs-lookup"><span data-stu-id="5bcff-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="5bcff-113">Ez a parancs letiltja a Contoso nevű külső végpontot az Erőforráscsoport11 erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="5bcff-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="5bcff-114">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bcff-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="5bcff-115">2. példa: Végpont letiltása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="5bcff-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="5bcff-116">Ez a parancs a Contoso nevű külső végpontot az ResourceGroup11 ContosoProfile nevű profiljából kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5bcff-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="5bcff-117">A parancs ezután átadja a végpontot a **Disable-AzTrafficManagerEndpoint** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="5bcff-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5bcff-118">Ez a parancsmag letiltja ezt a végpontot.</span><span class="sxs-lookup"><span data-stu-id="5bcff-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="5bcff-119">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bcff-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5bcff-120">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bcff-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5bcff-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bcff-121">PARAMETERS</span></span>

### <span data-ttu-id="5bcff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcff-122">-DefaultProfile</span></span>
<span data-ttu-id="5bcff-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bcff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bcff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5bcff-124">-Force</span></span>
<span data-ttu-id="5bcff-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5bcff-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5bcff-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5bcff-126">-Name</span></span>
<span data-ttu-id="5bcff-127">Annak a Traffic Manager-végpontnak a nevét adja meg, amelyről ez a parancsmag le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="5bcff-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="5bcff-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5bcff-128">-ProfileName</span></span>
<span data-ttu-id="5bcff-129">Annak a Traffic Manager-profilnak a nevét adja meg, amelyben ez a parancsmag letilt egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="5bcff-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="5bcff-130">Profil beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5bcff-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="5bcff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcff-131">-ResourceGroupName</span></span>
<span data-ttu-id="5bcff-132">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bcff-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5bcff-133">Ez a parancsmag letiltja a Traffic Manager-végpontot a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="5bcff-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5bcff-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5bcff-135">Azt a Traffic Manager-végpontot adja meg, amely letiltja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5bcff-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="5bcff-136">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5bcff-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="5bcff-137">-Type</span><span class="sxs-lookup"><span data-stu-id="5bcff-137">-Type</span></span>
<span data-ttu-id="5bcff-138">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="5bcff-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="5bcff-139">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="5bcff-139">Valid values are:</span></span> 

- <span data-ttu-id="5bcff-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="5bcff-140">AzureEndpoints</span></span>
- <span data-ttu-id="5bcff-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="5bcff-141">ExternalEndpoints</span></span>
- <span data-ttu-id="5bcff-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="5bcff-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="5bcff-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bcff-143">-Confirm</span></span>
<span data-ttu-id="5bcff-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bcff-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bcff-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bcff-145">-WhatIf</span></span>
<span data-ttu-id="5bcff-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5bcff-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bcff-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bcff-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bcff-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcff-148">CommonParameters</span></span>
<span data-ttu-id="5bcff-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bcff-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcff-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bcff-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcff-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bcff-151">INPUTS</span></span>

### <span data-ttu-id="5bcff-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5bcff-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bcff-153">OUTPUTS</span></span>

### <span data-ttu-id="5bcff-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bcff-154">System.Boolean</span></span>

## <span data-ttu-id="5bcff-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bcff-155">NOTES</span></span>

## <span data-ttu-id="5bcff-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bcff-156">RELATED LINKS</span></span>

[<span data-ttu-id="5bcff-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5bcff-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5bcff-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5bcff-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5bcff-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5bcff-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5bcff-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5bcff-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5bcff-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5bcff-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5bcff-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


