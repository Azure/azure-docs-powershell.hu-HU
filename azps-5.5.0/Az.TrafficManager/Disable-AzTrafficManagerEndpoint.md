---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165514"
---
# <span data-ttu-id="96d23-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="96d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96d23-102">SYNOPSIS</span></span>
<span data-ttu-id="96d23-103">Letilt egy végpontot egy Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="96d23-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="96d23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96d23-104">SYNTAX</span></span>

### <span data-ttu-id="96d23-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="96d23-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96d23-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="96d23-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96d23-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96d23-107">DESCRIPTION</span></span>
<span data-ttu-id="96d23-108">A **Disable-AzTrafficManagerEndpoint** parancsmag letilt egy végpontot egy Azure Traffic Manager-profilban.</span><span class="sxs-lookup"><span data-stu-id="96d23-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="96d23-109">A folyamat műveleti jelének használatával átadhat egy **TrafficManagerEndpoint-objektumot** ennek a parancsmagnak, vagy a **TrafficManagerEndpoint-objektumot** a *TrafficManagerEndpoint* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="96d23-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="96d23-110">Másik lehetőségként megadhatja a végpont nevét és típusát a Name *and* *Type* paraméter használatával, a *ProfileName* és *az ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="96d23-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="96d23-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96d23-111">EXAMPLES</span></span>

### <span data-ttu-id="96d23-112">1. példa: Végpont letiltása név szerint</span><span class="sxs-lookup"><span data-stu-id="96d23-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="96d23-113">Ez a parancs letiltja a Contoso nevű külső végpontot az Erőforráscsoport11 erőforráscsoport ContosoProfile nevű profiljában.</span><span class="sxs-lookup"><span data-stu-id="96d23-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="96d23-114">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96d23-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="96d23-115">2. példa: Végpont letiltása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="96d23-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="96d23-116">Ez a parancs a Contoso nevű külső végpontot az ResourceGroup11 ContosoProfile nevű profiljából kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96d23-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="96d23-117">A parancs ezután átadja a végpontot a **Disable-AzTrafficManagerEndpoint** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="96d23-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96d23-118">Ez a parancsmag letiltja ezt a végpontot.</span><span class="sxs-lookup"><span data-stu-id="96d23-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="96d23-119">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="96d23-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="96d23-120">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96d23-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="96d23-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96d23-121">PARAMETERS</span></span>

### <span data-ttu-id="96d23-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d23-122">-DefaultProfile</span></span>
<span data-ttu-id="96d23-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96d23-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96d23-124">-Force</span><span class="sxs-lookup"><span data-stu-id="96d23-124">-Force</span></span>
<span data-ttu-id="96d23-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="96d23-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96d23-126">-Name</span><span class="sxs-lookup"><span data-stu-id="96d23-126">-Name</span></span>
<span data-ttu-id="96d23-127">Annak a Traffic Manager-végpontnak a nevét adja meg, amelyről ez a parancsmag le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="96d23-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="96d23-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="96d23-128">-ProfileName</span></span>
<span data-ttu-id="96d23-129">Annak a Traffic Manager-profilnak a nevét adja meg, amelyben ez a parancsmag letilt egy végpontot.</span><span class="sxs-lookup"><span data-stu-id="96d23-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="96d23-130">Profil beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96d23-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="96d23-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d23-131">-ResourceGroupName</span></span>
<span data-ttu-id="96d23-132">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96d23-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="96d23-133">Ez a parancsmag letiltja a Traffic Manager-végpontot a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="96d23-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="96d23-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="96d23-135">Azt a Traffic Manager-végpontot adja meg, amely letiltja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96d23-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="96d23-136">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96d23-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="96d23-137">-Type</span><span class="sxs-lookup"><span data-stu-id="96d23-137">-Type</span></span>
<span data-ttu-id="96d23-138">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="96d23-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="96d23-139">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="96d23-139">Valid values are:</span></span> 

- <span data-ttu-id="96d23-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="96d23-140">AzureEndpoints</span></span>
- <span data-ttu-id="96d23-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="96d23-141">ExternalEndpoints</span></span>
- <span data-ttu-id="96d23-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="96d23-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="96d23-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96d23-143">-Confirm</span></span>
<span data-ttu-id="96d23-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96d23-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d23-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d23-145">-WhatIf</span></span>
<span data-ttu-id="96d23-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96d23-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96d23-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96d23-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d23-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d23-148">CommonParameters</span></span>
<span data-ttu-id="96d23-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d23-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d23-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d23-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d23-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96d23-151">INPUTS</span></span>

### <span data-ttu-id="96d23-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="96d23-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96d23-153">OUTPUTS</span></span>

### <span data-ttu-id="96d23-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96d23-154">System.Boolean</span></span>

## <span data-ttu-id="96d23-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96d23-155">NOTES</span></span>

## <span data-ttu-id="96d23-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96d23-156">RELATED LINKS</span></span>

[<span data-ttu-id="96d23-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96d23-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96d23-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96d23-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="96d23-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96d23-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96d23-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="96d23-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96d23-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96d23-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96d23-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


