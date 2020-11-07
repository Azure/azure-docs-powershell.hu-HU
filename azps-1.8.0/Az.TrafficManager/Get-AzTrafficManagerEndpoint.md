---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668404"
---
# <span data-ttu-id="1c6c4-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c6c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6c4-103">A forgalomirányító-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="1c6c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c6c4-104">SYNTAX</span></span>

### <span data-ttu-id="1c6c4-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="1c6c4-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c6c4-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="1c6c4-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c6c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6c4-108">A **Get-AzTrafficManagerEndpoint** parancsmag az Azure Traffic Manager-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1c6c4-109">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzTrafficManagerEndpoint parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="1c6c4-110">Adja meg a végpontot a *név* és a *típus* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="1c6c4-111">A Traffic Manager-profilt a *fájlnév* és a *ResourceGroupName* paraméter használatával, illetve egy **TrafficManagerProfile** objektum megadásával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1c6c4-112">Azt is megteheti, hogy a csővezetéken keresztül továbbítja ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="1c6c4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1c6c4-113">EXAMPLES</span></span>

### <span data-ttu-id="1c6c4-114">Példa 1: végpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="1c6c4-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="1c6c4-115">Ez a parancs a contoso nevű Azure-végpontot az ResourceGroup11 nevű ContosoProfile nevű profilból kapja, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="1c6c4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c6c4-116">PARAMETERS</span></span>

### <span data-ttu-id="1c6c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6c4-117">-DefaultProfile</span></span>
<span data-ttu-id="1c6c4-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c6c4-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c6c4-119">-Name</span></span>
<span data-ttu-id="1c6c4-120">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c6c4-121">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1c6c4-121">-ProfileName</span></span>
<span data-ttu-id="1c6c4-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c6c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c6c4-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1c6c4-125">Ez a parancsmag a forgalmi vezető végpontját kapja meg abban a csoportban, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c6c4-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1c6c4-127">Azt a forgalomirányítási végpontot adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c6c4-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="1c6c4-128">-Type</span></span>
<span data-ttu-id="1c6c4-129">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="1c6c4-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="1c6c4-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1c6c4-130">Valid values are:</span></span> 

- <span data-ttu-id="1c6c4-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c6c4-131">AzureEndpoints</span></span>
- <span data-ttu-id="1c6c4-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c6c4-132">ExternalEndpoints</span></span>
- <span data-ttu-id="1c6c4-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c6c4-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="1c6c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6c4-134">CommonParameters</span></span>
<span data-ttu-id="1c6c4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c6c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6c4-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6c4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6c4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6c4-137">INPUTS</span></span>

### <span data-ttu-id="1c6c4-138">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c6c4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c6c4-139">OUTPUTS</span></span>

### <span data-ttu-id="1c6c4-140">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c6c4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c6c4-141">NOTES</span></span>

## <span data-ttu-id="1c6c4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c6c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="1c6c4-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c6c4-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c6c4-145">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c6c4-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c6c4-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c6c4-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


