---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495218"
---
# <span data-ttu-id="6c334-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c334-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6c334-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c334-102">SYNOPSIS</span></span>
<span data-ttu-id="6c334-103">Végpont eltávolítása a Traffic Managerből.</span><span class="sxs-lookup"><span data-stu-id="6c334-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c334-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c334-104">SYNTAX</span></span>

### <span data-ttu-id="6c334-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="6c334-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c334-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="6c334-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c334-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c334-107">DESCRIPTION</span></span>
<span data-ttu-id="6c334-108">A **Remove-AzureRmTrafficManagerEndpoint** parancsmag eltávolítja az Azure Traffic Manager végpontját.</span><span class="sxs-lookup"><span data-stu-id="6c334-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="6c334-109">Ez a parancsmag minden módosítást véglegesít a Traffic Manager szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="6c334-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="6c334-110">Ha több végpontot szeretne eltávolítani egy helyi forgalomirányítási profil-objektumból, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Remove-AzureRmTrafficManagerEndpointConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c334-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="6c334-111">A pipeline operátor segítségével átadhatja a **TrafficManagerEndpoint** -objektumokat a parancsmagnak, vagy megadhat egy **TrafficManagerEndpoint** -objektumot a *TrafficManagerEndpoint* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="6c334-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="6c334-112">Azt is megteheti, hogy megadhatja a végpont nevét és típusát a *név* és a *típus* paraméterrel együtt, a *fájl* -és *ResourceGroupName* paraméterekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="6c334-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="6c334-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6c334-113">EXAMPLES</span></span>

### <span data-ttu-id="6c334-114">Példa 1: végpont eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="6c334-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="6c334-115">Ez a parancs eltávolítja a contoso nevű Azure-végpontot az ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljából.</span><span class="sxs-lookup"><span data-stu-id="6c334-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="6c334-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c334-116">PARAMETERS</span></span>

### <span data-ttu-id="6c334-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c334-117">-DefaultProfile</span></span>
<span data-ttu-id="6c334-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c334-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c334-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6c334-119">-Force</span></span>
<span data-ttu-id="6c334-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6c334-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c334-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c334-121">-Name</span></span>
<span data-ttu-id="6c334-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6c334-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c334-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="6c334-123">-ProfileName</span></span>
<span data-ttu-id="6c334-124">Annak a forgalomirányító-profilnak a neve, amelyből a parancsmag eltávolítja a végpontot.</span><span class="sxs-lookup"><span data-stu-id="6c334-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="6c334-125">Ha profilt szeretne beolvasni, használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c334-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6c334-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c334-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c334-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c334-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6c334-128">Ez a parancsmag a forgalomirányító végpontját eltávolítja a forgalomirányító-profilból abban a csoportban, amelyben ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c334-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c334-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c334-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6c334-130">A forgalomirányító végpontját adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="6c334-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="6c334-131">**TrafficManagerEndpoint** objektum beolvasásához használja az Get-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c334-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6c334-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="6c334-132">-Type</span></span>
<span data-ttu-id="6c334-133">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="6c334-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="6c334-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6c334-134">Valid values are:</span></span> 

- <span data-ttu-id="6c334-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c334-135">AzureEndpoints</span></span>
- <span data-ttu-id="6c334-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c334-136">ExternalEndpoints</span></span>
- <span data-ttu-id="6c334-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c334-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="6c334-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c334-138">-Confirm</span></span>
<span data-ttu-id="6c334-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c334-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c334-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c334-140">-WhatIf</span></span>
<span data-ttu-id="6c334-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c334-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c334-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c334-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c334-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c334-143">CommonParameters</span></span>
<span data-ttu-id="6c334-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c334-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c334-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c334-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c334-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c334-146">INPUTS</span></span>

### <span data-ttu-id="6c334-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c334-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="6c334-148">A ' TrafficManagerEndpoint ' paraméter az "TrafficManagerEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6c334-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="6c334-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c334-149">OUTPUTS</span></span>

### <span data-ttu-id="6c334-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c334-150">System.Boolean</span></span>

## <span data-ttu-id="6c334-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c334-151">NOTES</span></span>

## <span data-ttu-id="6c334-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c334-152">RELATED LINKS</span></span>

[<span data-ttu-id="6c334-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c334-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6c334-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c334-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6c334-155">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c334-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6c334-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6c334-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6c334-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c334-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


