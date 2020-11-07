---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672050"
---
# <span data-ttu-id="638d8-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="638d8-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="638d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="638d8-102">SYNOPSIS</span></span>
<span data-ttu-id="638d8-103">Eltávolítja a végpontot egy helyi forgalomirányító-profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="638d8-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="638d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="638d8-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638d8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="638d8-105">DESCRIPTION</span></span>
<span data-ttu-id="638d8-106">A **Remove-AzureRmTrafficManagerEndpointConfig** parancsmag eltávolítja a végpontot egy helyi Azure Traffic Manager-profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="638d8-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="638d8-107">A Get-AzureRmTrafficManagerProfile parancsmag használatával is beszerezhet egy profilt.</span><span class="sxs-lookup"><span data-stu-id="638d8-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="638d8-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="638d8-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="638d8-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="638d8-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="638d8-110">Ha el szeretne távolítani egy végpontot, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Remove-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="638d8-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="638d8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="638d8-111">EXAMPLES</span></span>

### <span data-ttu-id="638d8-112">1. példa: végpont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="638d8-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="638d8-113">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="638d8-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="638d8-114">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="638d8-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="638d8-115">A második parancs eltávolítja a contoso nevű Azure-végpontot az $TrafficManagerProfile tárolt profilból.</span><span class="sxs-lookup"><span data-stu-id="638d8-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="638d8-116">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="638d8-116">This command changes only the local object.</span></span>

<span data-ttu-id="638d8-117">A végleges parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="638d8-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="638d8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="638d8-118">PARAMETERS</span></span>

### <span data-ttu-id="638d8-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="638d8-119">-EndpointName</span></span>
<span data-ttu-id="638d8-120">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="638d8-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638d8-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="638d8-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="638d8-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="638d8-123">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="638d8-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="638d8-124">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="638d8-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="638d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-125">-DefaultProfile</span></span>
<span data-ttu-id="638d8-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="638d8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="638d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638d8-127">CommonParameters</span></span>
<span data-ttu-id="638d8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="638d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638d8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638d8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="638d8-130">INPUTS</span></span>

### <span data-ttu-id="638d8-131">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="638d8-132">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="638d8-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="638d8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="638d8-133">OUTPUTS</span></span>

### <span data-ttu-id="638d8-134">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="638d8-135">Ez a parancsmag egy módosított TrafficManagerProfile objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="638d8-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="638d8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="638d8-136">NOTES</span></span>

## <span data-ttu-id="638d8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="638d8-137">RELATED LINKS</span></span>

[<span data-ttu-id="638d8-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="638d8-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="638d8-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="638d8-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="638d8-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="638d8-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="638d8-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


