---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 196cdd5f41a33fe0e4185c4f30a35ce9444139de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668409"
---
# <span data-ttu-id="343bd-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="343bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="343bd-102">SYNOPSIS</span></span>
<span data-ttu-id="343bd-103">Letiltja egy végpontot egy forgalomirányítási profilban.</span><span class="sxs-lookup"><span data-stu-id="343bd-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="343bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="343bd-104">SYNTAX</span></span>

### <span data-ttu-id="343bd-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="343bd-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="343bd-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="343bd-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="343bd-107">DESCRIPTION</span></span>
<span data-ttu-id="343bd-108">A **disable-AzTrafficManagerEndpoint** parancsmag letiltja az Azure Traffic Manager-profilok végpontját.</span><span class="sxs-lookup"><span data-stu-id="343bd-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="343bd-109">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy átadhat egy **TrafficManagerEndpoint** objektumot a *TrafficManagerEndpoint* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="343bd-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="343bd-110">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="343bd-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="343bd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="343bd-111">EXAMPLES</span></span>

### <span data-ttu-id="343bd-112">Példa 1: végpont letiltása név szerint</span><span class="sxs-lookup"><span data-stu-id="343bd-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="343bd-113">Ez a parancs letiltja a contoso nevű külső végpontot az erőforráscsoport ResouceGroup11 a ContosoProfile nevű profilban.</span><span class="sxs-lookup"><span data-stu-id="343bd-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="343bd-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="343bd-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="343bd-115">2. példa: végpont letiltása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="343bd-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="343bd-116">Ez a parancs a contoso nevű külső végpontot a ResourceGroup11 nevű ContosoProfile-profilból kapja.</span><span class="sxs-lookup"><span data-stu-id="343bd-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="343bd-117">Ekkor a parancs átadja ezt a végpontot a **letiltási AzTrafficManagerEndpoint** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="343bd-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="343bd-118">A parancsmag letiltja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="343bd-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="343bd-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="343bd-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="343bd-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="343bd-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="343bd-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="343bd-121">PARAMETERS</span></span>

### <span data-ttu-id="343bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343bd-122">-DefaultProfile</span></span>
<span data-ttu-id="343bd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="343bd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343bd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="343bd-124">-Force</span></span>
<span data-ttu-id="343bd-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="343bd-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="343bd-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="343bd-126">-Name</span></span>
<span data-ttu-id="343bd-127">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="343bd-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="343bd-128">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="343bd-128">-ProfileName</span></span>
<span data-ttu-id="343bd-129">Annak a forgalomirányító-profilnak a nevét adja meg, amelyben a parancsmag letiltja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="343bd-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="343bd-130">Ha profilt szeretne beolvasni, használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="343bd-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="343bd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343bd-131">-ResourceGroupName</span></span>
<span data-ttu-id="343bd-132">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="343bd-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="343bd-133">Ez a parancsmag letiltja a Traffic Manager végpontját abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="343bd-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="343bd-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="343bd-135">A forgalomirányítási végpontot adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="343bd-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="343bd-136">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="343bd-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="343bd-137">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="343bd-137">-Type</span></span>
<span data-ttu-id="343bd-138">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="343bd-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="343bd-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="343bd-139">Valid values are:</span></span> 

- <span data-ttu-id="343bd-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="343bd-140">AzureEndpoints</span></span>
- <span data-ttu-id="343bd-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="343bd-141">ExternalEndpoints</span></span>
- <span data-ttu-id="343bd-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="343bd-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="343bd-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="343bd-143">-Confirm</span></span>
<span data-ttu-id="343bd-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="343bd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343bd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343bd-145">-WhatIf</span></span>
<span data-ttu-id="343bd-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="343bd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343bd-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="343bd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343bd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343bd-148">CommonParameters</span></span>
<span data-ttu-id="343bd-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="343bd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343bd-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343bd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343bd-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="343bd-151">INPUTS</span></span>

### <span data-ttu-id="343bd-152">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="343bd-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="343bd-153">OUTPUTS</span></span>

### <span data-ttu-id="343bd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="343bd-154">System.Boolean</span></span>

## <span data-ttu-id="343bd-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="343bd-155">NOTES</span></span>

## <span data-ttu-id="343bd-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="343bd-156">RELATED LINKS</span></span>

[<span data-ttu-id="343bd-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="343bd-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="343bd-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="343bd-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="343bd-160">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="343bd-161">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="343bd-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="343bd-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="343bd-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="343bd-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="343bd-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


