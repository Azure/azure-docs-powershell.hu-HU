---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 13b798da7b35a4721b35d2375cf4e25bb47fbb98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678914"
---
# <span data-ttu-id="b9886-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b9886-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9886-102">SYNOPSIS</span></span>
<span data-ttu-id="b9886-103">Letiltja egy végpontot egy forgalomirányítási profilban.</span><span class="sxs-lookup"><span data-stu-id="b9886-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9886-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9886-104">SYNTAX</span></span>

### <span data-ttu-id="b9886-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="b9886-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9886-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="b9886-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9886-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9886-107">DESCRIPTION</span></span>
<span data-ttu-id="b9886-108">A **disable-AzureRmTrafficManagerEndpoint** parancsmag letiltja az Azure Traffic Manager-profilok végpontját.</span><span class="sxs-lookup"><span data-stu-id="b9886-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b9886-109">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy átadhat egy **TrafficManagerEndpoint** objektumot a *TrafficManagerEndpoint* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="b9886-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="b9886-110">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="b9886-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="b9886-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b9886-111">EXAMPLES</span></span>

### <span data-ttu-id="b9886-112">Példa 1: végpont letiltása név szerint</span><span class="sxs-lookup"><span data-stu-id="b9886-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="b9886-113">Ez a parancs letiltja a contoso nevű külső végpontot az erőforráscsoport ResouceGroup11 a ContosoProfile nevű profilban.</span><span class="sxs-lookup"><span data-stu-id="b9886-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="b9886-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="b9886-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b9886-115">2. példa: végpont letiltása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="b9886-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="b9886-116">Ez a parancs a contoso nevű külső végpontot a ResourceGroup11 nevű ContosoProfile-profilból kapja.</span><span class="sxs-lookup"><span data-stu-id="b9886-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b9886-117">Ekkor a parancs átadja ezt a végpontot a **letiltási AzureRmTrafficManagerEndpoint** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="b9886-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b9886-118">A parancsmag letiltja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="b9886-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="b9886-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9886-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b9886-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9886-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b9886-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9886-121">PARAMETERS</span></span>

### <span data-ttu-id="b9886-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9886-122">-DefaultProfile</span></span>
<span data-ttu-id="b9886-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9886-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9886-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b9886-124">-Force</span></span>
<span data-ttu-id="b9886-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b9886-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9886-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9886-126">-Name</span></span>
<span data-ttu-id="b9886-127">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="b9886-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-128">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="b9886-128">-ProfileName</span></span>
<span data-ttu-id="b9886-129">Annak a forgalomirányító-profilnak a nevét adja meg, amelyben a parancsmag letiltja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="b9886-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="b9886-130">Ha profilt szeretne beolvasni, használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b9886-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9886-131">-ResourceGroupName</span></span>
<span data-ttu-id="b9886-132">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9886-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b9886-133">Ez a parancsmag letiltja a Traffic Manager végpontját abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b9886-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b9886-135">A forgalomirányítási végpontot adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="b9886-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="b9886-136">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b9886-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-137">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="b9886-137">-Type</span></span>
<span data-ttu-id="b9886-138">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="b9886-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b9886-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b9886-139">Valid values are:</span></span> 

- <span data-ttu-id="b9886-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b9886-140">AzureEndpoints</span></span>
- <span data-ttu-id="b9886-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b9886-141">ExternalEndpoints</span></span>
- <span data-ttu-id="b9886-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b9886-142">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9886-143">-Confirm</span></span>
<span data-ttu-id="b9886-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9886-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9886-145">-WhatIf</span></span>
<span data-ttu-id="b9886-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9886-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9886-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9886-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9886-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9886-148">CommonParameters</span></span>
<span data-ttu-id="b9886-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9886-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9886-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9886-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9886-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9886-151">INPUTS</span></span>

### <span data-ttu-id="b9886-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="b9886-153">A ' TrafficManagerEndpoint ' paraméter az "TrafficManagerEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b9886-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="b9886-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9886-154">OUTPUTS</span></span>

### <span data-ttu-id="b9886-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9886-155">System.Boolean</span></span>

## <span data-ttu-id="b9886-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9886-156">NOTES</span></span>

## <span data-ttu-id="b9886-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9886-157">RELATED LINKS</span></span>

[<span data-ttu-id="b9886-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b9886-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b9886-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b9886-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b9886-161">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b9886-162">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b9886-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b9886-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b9886-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b9886-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b9886-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


