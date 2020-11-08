---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011651"
---
# <span data-ttu-id="b11d1-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="b11d1-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="b11d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b11d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b11d1-103">A helyi forgalmi igazgató profil objektumhoz hozzáadja a várható állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="b11d1-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="b11d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b11d1-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b11d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b11d1-105">DESCRIPTION</span></span>
<span data-ttu-id="b11d1-106">Az **Add-AzTrafficManagerExpectedStatusCodeRange** parancsmag egy, a helyi Azure Traffic Manager-profil objektumba felvett, a várt állapotkódok tartományát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b11d1-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b11d1-107">A New-AzTrafficManagerProfile-vagy Get-AzTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="b11d1-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="b11d1-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="b11d1-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b11d1-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b11d1-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="b11d1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b11d1-110">EXAMPLES</span></span>

### <span data-ttu-id="b11d1-111">1. példa: a várt állapotkódot tartalmazó tartományok felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="b11d1-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b11d1-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b11d1-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b11d1-113">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="b11d1-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="b11d1-114">A második parancs hozzáadja a várt állapotkódot az $TrafficManagerProfile tárolt profilhoz.</span><span class="sxs-lookup"><span data-stu-id="b11d1-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b11d1-115">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b11d1-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b11d1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b11d1-116">PARAMETERS</span></span>

### <span data-ttu-id="b11d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-117">-DefaultProfile</span></span>
<span data-ttu-id="b11d1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b11d1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11d1-119">-Max</span><span class="sxs-lookup"><span data-stu-id="b11d1-119">-Max</span></span>
<span data-ttu-id="b11d1-120">A felvenni kívánt állapotkód-intervallum legmagasabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b11d1-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11d1-121">-Min</span><span class="sxs-lookup"><span data-stu-id="b11d1-121">-Min</span></span>
<span data-ttu-id="b11d1-122">A hozzáadandó állapotkód-tartományok legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b11d1-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11d1-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b11d1-124">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b11d1-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b11d1-125">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="b11d1-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b11d1-126">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b11d1-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b11d1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b11d1-127">-Confirm</span></span>
<span data-ttu-id="b11d1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b11d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11d1-129">-WhatIf</span></span>
<span data-ttu-id="b11d1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b11d1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b11d1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b11d1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11d1-132">CommonParameters</span></span>
<span data-ttu-id="b11d1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b11d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11d1-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11d1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11d1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b11d1-135">INPUTS</span></span>

### <span data-ttu-id="b11d1-136">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b11d1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b11d1-137">OUTPUTS</span></span>

### <span data-ttu-id="b11d1-138">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b11d1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b11d1-139">NOTES</span></span>

## <span data-ttu-id="b11d1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b11d1-140">RELATED LINKS</span></span>

[<span data-ttu-id="b11d1-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="b11d1-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="b11d1-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b11d1-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b11d1-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
