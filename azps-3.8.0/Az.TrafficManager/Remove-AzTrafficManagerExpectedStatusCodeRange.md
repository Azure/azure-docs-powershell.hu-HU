---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012600"
---
# <span data-ttu-id="62ad0-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="62ad0-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="62ad0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="62ad0-103">Eltávolítja a várt állapotkódot a helyi forgalomirányítási profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="62ad0-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="62ad0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62ad0-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ad0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="62ad0-106">A **Remove-AzTrafficManagerExpectedStatusCodeRange** parancsmag egy helyi Azure Traffic Manager-profil objektumból távolítja el a várt állapotkódok tartományát.</span><span class="sxs-lookup"><span data-stu-id="62ad0-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="62ad0-107">A New-AzTrafficManagerProfile-vagy Get-AzTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="62ad0-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="62ad0-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="62ad0-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="62ad0-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="62ad0-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="62ad0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62ad0-110">EXAMPLES</span></span>

### <span data-ttu-id="62ad0-111">1. példa: a várt állapotkódot tartalmazó tartományok eltávolítása a profilból</span><span class="sxs-lookup"><span data-stu-id="62ad0-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="62ad0-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62ad0-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="62ad0-113">A második parancs eltávolítja a $TrafficManagerProfileban tárolt profilból a várt állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="62ad0-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="62ad0-114">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="62ad0-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="62ad0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62ad0-115">PARAMETERS</span></span>

### <span data-ttu-id="62ad0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-116">-DefaultProfile</span></span>
<span data-ttu-id="62ad0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62ad0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ad0-118">-Min</span><span class="sxs-lookup"><span data-stu-id="62ad0-118">-Min</span></span>
<span data-ttu-id="62ad0-119">Az állapotkód eltávolításának legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62ad0-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="62ad0-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="62ad0-121">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="62ad0-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="62ad0-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="62ad0-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="62ad0-123">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="62ad0-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="62ad0-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62ad0-124">-Confirm</span></span>
<span data-ttu-id="62ad0-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62ad0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ad0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ad0-126">-WhatIf</span></span>
<span data-ttu-id="62ad0-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62ad0-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62ad0-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62ad0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ad0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ad0-129">CommonParameters</span></span>
<span data-ttu-id="62ad0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62ad0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ad0-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ad0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ad0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ad0-132">INPUTS</span></span>

### <span data-ttu-id="62ad0-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="62ad0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ad0-134">OUTPUTS</span></span>

### <span data-ttu-id="62ad0-135">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="62ad0-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62ad0-136">NOTES</span></span>

## <span data-ttu-id="62ad0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62ad0-137">RELATED LINKS</span></span>

[<span data-ttu-id="62ad0-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="62ad0-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="62ad0-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="62ad0-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad0-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
