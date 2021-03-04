---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 04764a27a6940c0bc2b5d0e6df0baad350606972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918002"
---
# <span data-ttu-id="122f6-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="122f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122f6-102">SYNOPSIS</span></span>
<span data-ttu-id="122f6-103">Egy Traffic Manager-profil végpontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="122f6-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="122f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="122f6-104">SYNTAX</span></span>

### <span data-ttu-id="122f6-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="122f6-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="122f6-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="122f6-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="122f6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="122f6-107">DESCRIPTION</span></span>
<span data-ttu-id="122f6-108">A **Get-AzTrafficManagerEndpoint** parancsmag egy Azure Traffic Manager-profil végpontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="122f6-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="122f6-109">Ezt az objektumot helyben módosíthatja, majd a profilon a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="122f6-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="122f6-110">Adja meg a végpontot a Név *és* a *Típus paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="122f6-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="122f6-111">A Traffic Manager-profilt a *ProfileName* és *az ResourceGroupName* paraméterrel, illetve a **TrafficManagerProfile** objektum megadásával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="122f6-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="122f6-112">Másik lehetőségként át is használhatja ezt az értéket a folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="122f6-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="122f6-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="122f6-113">EXAMPLES</span></span>

### <span data-ttu-id="122f6-114">1. példa: Végpont lekérte</span><span class="sxs-lookup"><span data-stu-id="122f6-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="122f6-115">Ez a parancs a Contoso nevű Azure-végpontot az ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljából kapja meg, majd az objektumot a $TrafficManagerEndpoint tárolja.</span><span class="sxs-lookup"><span data-stu-id="122f6-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="122f6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="122f6-116">PARAMETERS</span></span>

### <span data-ttu-id="122f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122f6-117">-DefaultProfile</span></span>
<span data-ttu-id="122f6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="122f6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="122f6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="122f6-119">-Name</span></span>
<span data-ttu-id="122f6-120">Megadja annak a Traffic Manager-végpontnak a nevét, amelybe ez a parancsmag be fog jut.</span><span class="sxs-lookup"><span data-stu-id="122f6-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="122f6-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="122f6-121">-ProfileName</span></span>
<span data-ttu-id="122f6-122">Megadja annak a Traffic Manager-végpontnak a nevét, amelybe ez a parancsmag be fog jut.</span><span class="sxs-lookup"><span data-stu-id="122f6-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="122f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="122f6-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="122f6-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="122f6-125">Ez a parancsmag egy Traffic Manager-végpontot kap a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="122f6-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="122f6-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="122f6-127">Azt a Traffic Manager-végpontot adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="122f6-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="122f6-128">-Type</span><span class="sxs-lookup"><span data-stu-id="122f6-128">-Type</span></span>
<span data-ttu-id="122f6-129">Megadja, hogy a parancsmag milyen típusú végpontot ad hozzá a Traffic Manager-profilhoz.</span><span class="sxs-lookup"><span data-stu-id="122f6-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="122f6-130">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="122f6-130">Valid values are:</span></span> 

- <span data-ttu-id="122f6-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="122f6-131">AzureEndpoints</span></span>
- <span data-ttu-id="122f6-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="122f6-132">ExternalEndpoints</span></span>
- <span data-ttu-id="122f6-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="122f6-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="122f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122f6-134">CommonParameters</span></span>
<span data-ttu-id="122f6-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122f6-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122f6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122f6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="122f6-137">INPUTS</span></span>

### <span data-ttu-id="122f6-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="122f6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="122f6-139">OUTPUTS</span></span>

### <span data-ttu-id="122f6-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="122f6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="122f6-141">NOTES</span></span>

## <span data-ttu-id="122f6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="122f6-142">RELATED LINKS</span></span>

[<span data-ttu-id="122f6-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="122f6-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="122f6-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="122f6-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="122f6-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="122f6-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


