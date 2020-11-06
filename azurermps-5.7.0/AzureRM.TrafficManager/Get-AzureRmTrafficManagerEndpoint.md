---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500339"
---
# <span data-ttu-id="7aff3-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7aff3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7aff3-102">SYNOPSIS</span></span>
<span data-ttu-id="7aff3-103">A forgalomirányító-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="7aff3-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aff3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7aff3-104">SYNTAX</span></span>

### <span data-ttu-id="7aff3-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="7aff3-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7aff3-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="7aff3-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aff3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7aff3-107">DESCRIPTION</span></span>
<span data-ttu-id="7aff3-108">A **Get-AzureRmTrafficManagerEndpoint** parancsmag az Azure Traffic Manager-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="7aff3-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="7aff3-109">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmTrafficManagerEndpoint parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="7aff3-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="7aff3-110">Adja meg a végpontot a *név* és a *típus* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="7aff3-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="7aff3-111">A Traffic Manager-profilt a *fájlnév* és a *ResourceGroupName* paraméter használatával, illetve egy **TrafficManagerProfile** objektum megadásával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="7aff3-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7aff3-112">Azt is megteheti, hogy a csővezetéken keresztül továbbítja ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="7aff3-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="7aff3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7aff3-113">EXAMPLES</span></span>

### <span data-ttu-id="7aff3-114">Példa 1: végpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="7aff3-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="7aff3-115">Ez a parancs a contoso nevű Azure-végpontot az ResourceGroup11 nevű ContosoProfile nevű profilból kapja, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7aff3-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="7aff3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7aff3-116">PARAMETERS</span></span>

### <span data-ttu-id="7aff3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aff3-117">-DefaultProfile</span></span>
<span data-ttu-id="7aff3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7aff3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aff3-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7aff3-119">-Name</span></span>
<span data-ttu-id="7aff3-120">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7aff3-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aff3-121">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7aff3-121">-ProfileName</span></span>
<span data-ttu-id="7aff3-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7aff3-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aff3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aff3-123">-ResourceGroupName</span></span>
<span data-ttu-id="7aff3-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aff3-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7aff3-125">Ez a parancsmag a forgalmi vezető végpontját kapja meg abban a csoportban, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aff3-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7aff3-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7aff3-127">Azt a forgalomirányítási végpontot adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7aff3-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aff3-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="7aff3-128">-Type</span></span>
<span data-ttu-id="7aff3-129">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="7aff3-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="7aff3-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7aff3-130">Valid values are:</span></span> 

- <span data-ttu-id="7aff3-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="7aff3-131">AzureEndpoints</span></span>
- <span data-ttu-id="7aff3-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="7aff3-132">ExternalEndpoints</span></span>
- <span data-ttu-id="7aff3-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="7aff3-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="7aff3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aff3-134">CommonParameters</span></span>
<span data-ttu-id="7aff3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7aff3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aff3-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aff3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aff3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aff3-137">INPUTS</span></span>

### <span data-ttu-id="7aff3-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="7aff3-139">A ' TrafficManagerEndpoint ' paraméter az "TrafficManagerEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7aff3-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7aff3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aff3-140">OUTPUTS</span></span>

### <span data-ttu-id="7aff3-141">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7aff3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7aff3-142">NOTES</span></span>

## <span data-ttu-id="7aff3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aff3-143">RELATED LINKS</span></span>

[<span data-ttu-id="7aff3-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7aff3-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7aff3-146">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7aff3-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7aff3-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7aff3-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


