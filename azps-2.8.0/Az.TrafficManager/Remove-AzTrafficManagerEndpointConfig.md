---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839949"
---
# <span data-ttu-id="66d9f-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="66d9f-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="66d9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="66d9f-103">Eltávolítja a végpontot egy helyi forgalomirányító-profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="66d9f-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="66d9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66d9f-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="66d9f-106">A **Remove-AzTrafficManagerEndpointConfig** parancsmag eltávolítja a végpontot egy helyi Azure Traffic Manager-profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="66d9f-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="66d9f-107">A Get-AzTrafficManagerProfile parancsmag használatával is beszerezhet egy profilt.</span><span class="sxs-lookup"><span data-stu-id="66d9f-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="66d9f-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="66d9f-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="66d9f-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="66d9f-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="66d9f-110">Ha el szeretne távolítani egy végpontot, és egyetlen műveletben szeretne módosításokat végrehajtani, használja az Remove-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="66d9f-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="66d9f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66d9f-111">EXAMPLES</span></span>

### <span data-ttu-id="66d9f-112">1. példa: végpont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="66d9f-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="66d9f-113">Az első parancs az Azure Traffic Manager-profilt a **Get-AzTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66d9f-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="66d9f-114">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="66d9f-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="66d9f-115">A második parancs eltávolítja a contoso nevű Azure-végpontot az $TrafficManagerProfile tárolt profilból.</span><span class="sxs-lookup"><span data-stu-id="66d9f-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="66d9f-116">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="66d9f-116">This command changes only the local object.</span></span>

<span data-ttu-id="66d9f-117">A végleges parancs frissíti a ContosoProfile nevű forgalomirányítási profilt az $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="66d9f-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="66d9f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66d9f-118">PARAMETERS</span></span>

### <span data-ttu-id="66d9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-119">-DefaultProfile</span></span>
<span data-ttu-id="66d9f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66d9f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66d9f-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="66d9f-121">-EndpointName</span></span>
<span data-ttu-id="66d9f-122">Annak a forgalmi vezető végpontnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="66d9f-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66d9f-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="66d9f-124">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="66d9f-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="66d9f-125">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="66d9f-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="66d9f-126">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="66d9f-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="66d9f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d9f-127">CommonParameters</span></span>
<span data-ttu-id="66d9f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66d9f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d9f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d9f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d9f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d9f-130">INPUTS</span></span>

### <span data-ttu-id="66d9f-131">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="66d9f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d9f-132">OUTPUTS</span></span>

### <span data-ttu-id="66d9f-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="66d9f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66d9f-134">NOTES</span></span>

## <span data-ttu-id="66d9f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66d9f-135">RELATED LINKS</span></span>

[<span data-ttu-id="66d9f-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="66d9f-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="66d9f-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="66d9f-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66d9f-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="66d9f-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


