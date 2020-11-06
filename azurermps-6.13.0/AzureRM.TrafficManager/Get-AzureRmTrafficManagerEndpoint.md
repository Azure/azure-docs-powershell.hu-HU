---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 335cb4308a64811fdc99b0bafe6660ee69c9b9d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497211"
---
# <span data-ttu-id="f0108-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f0108-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0108-102">SYNOPSIS</span></span>
<span data-ttu-id="f0108-103">A forgalomirányító-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="f0108-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0108-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0108-104">SYNTAX</span></span>

### <span data-ttu-id="f0108-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="f0108-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0108-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="f0108-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0108-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0108-107">DESCRIPTION</span></span>
<span data-ttu-id="f0108-108">A **Get-AzureRmTrafficManagerEndpoint** parancsmag az Azure Traffic Manager-profil végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="f0108-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="f0108-109">Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmTrafficManagerEndpoint parancsmag használatával alkalmazhatja a profil módosításait.</span><span class="sxs-lookup"><span data-stu-id="f0108-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="f0108-110">Adja meg a végpontot a *név* és a *típus* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="f0108-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="f0108-111">A Traffic Manager-profilt a *fájlnév* és a *ResourceGroupName* paraméter használatával, illetve egy **TrafficManagerProfile** objektum megadásával adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="f0108-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f0108-112">Azt is megteheti, hogy a csővezetéken keresztül továbbítja ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="f0108-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="f0108-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f0108-113">EXAMPLES</span></span>

### <span data-ttu-id="f0108-114">Példa 1: végpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0108-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="f0108-115">Ez a parancs a contoso nevű Azure-végpontot az ResourceGroup11 nevű ContosoProfile nevű profilból kapja, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f0108-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="f0108-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0108-116">PARAMETERS</span></span>

### <span data-ttu-id="f0108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0108-117">-DefaultProfile</span></span>
<span data-ttu-id="f0108-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0108-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0108-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0108-119">-Name</span></span>
<span data-ttu-id="f0108-120">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="f0108-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0108-121">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="f0108-121">-ProfileName</span></span>
<span data-ttu-id="f0108-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="f0108-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0108-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0108-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0108-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0108-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f0108-125">Ez a parancsmag a forgalmi vezető végpontját kapja meg abban a csoportban, amelyre ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0108-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0108-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f0108-127">Azt a forgalomirányítási végpontot adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f0108-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0108-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f0108-128">-Type</span></span>
<span data-ttu-id="f0108-129">Azt adja meg, hogy milyen típusú végpontot ad a parancsmag a forgalomirányítási profilhoz.</span><span class="sxs-lookup"><span data-stu-id="f0108-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="f0108-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f0108-130">Valid values are:</span></span> 

- <span data-ttu-id="f0108-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f0108-131">AzureEndpoints</span></span>
- <span data-ttu-id="f0108-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f0108-132">ExternalEndpoints</span></span>
- <span data-ttu-id="f0108-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f0108-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="f0108-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0108-134">CommonParameters</span></span>
<span data-ttu-id="f0108-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0108-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0108-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0108-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0108-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0108-137">INPUTS</span></span>

### <span data-ttu-id="f0108-138">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>
<span data-ttu-id="f0108-139">A ' TrafficManagerEndpoint ' paraméter az "TrafficManagerEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f0108-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f0108-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0108-140">OUTPUTS</span></span>

### <span data-ttu-id="f0108-141">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f0108-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0108-142">NOTES</span></span>

## <span data-ttu-id="f0108-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0108-143">RELATED LINKS</span></span>

[<span data-ttu-id="f0108-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f0108-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f0108-146">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f0108-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f0108-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0108-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


