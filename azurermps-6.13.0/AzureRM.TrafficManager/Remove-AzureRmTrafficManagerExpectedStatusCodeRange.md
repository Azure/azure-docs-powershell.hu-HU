---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492678"
---
# <span data-ttu-id="ae76e-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ae76e-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="ae76e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae76e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae76e-103">Eltávolítja a várt állapotkódot a helyi forgalomirányítási profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="ae76e-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae76e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae76e-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae76e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae76e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae76e-106">A **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** parancsmag egy helyi Azure Traffic Manager-profil objektumból távolítja el a várt állapotkódok tartományát.</span><span class="sxs-lookup"><span data-stu-id="ae76e-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ae76e-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="ae76e-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ae76e-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="ae76e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ae76e-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="ae76e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ae76e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ae76e-110">EXAMPLES</span></span>

### <span data-ttu-id="ae76e-111">1. példa: a várt állapotkódot tartalmazó tartományok eltávolítása a profilból</span><span class="sxs-lookup"><span data-stu-id="ae76e-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ae76e-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae76e-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ae76e-113">A második parancs eltávolítja a $TrafficManagerProfileban tárolt profilból a várt állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="ae76e-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ae76e-114">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="ae76e-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ae76e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae76e-115">PARAMETERS</span></span>

### <span data-ttu-id="ae76e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-116">-DefaultProfile</span></span>
<span data-ttu-id="ae76e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae76e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae76e-118">-Min</span><span class="sxs-lookup"><span data-stu-id="ae76e-118">-Min</span></span>
<span data-ttu-id="ae76e-119">Az állapotkód eltávolításának legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae76e-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="ae76e-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="ae76e-121">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ae76e-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ae76e-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="ae76e-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ae76e-123">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ae76e-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ae76e-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae76e-124">-Confirm</span></span>
<span data-ttu-id="ae76e-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae76e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae76e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae76e-126">-WhatIf</span></span>
<span data-ttu-id="ae76e-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae76e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae76e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae76e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae76e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae76e-129">CommonParameters</span></span>
<span data-ttu-id="ae76e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae76e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae76e-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae76e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae76e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae76e-132">INPUTS</span></span>

### <span data-ttu-id="ae76e-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ae76e-134">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="ae76e-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="ae76e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae76e-135">OUTPUTS</span></span>

### <span data-ttu-id="ae76e-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ae76e-137">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ae76e-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="ae76e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae76e-138">NOTES</span></span>

## <span data-ttu-id="ae76e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae76e-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae76e-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ae76e-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="ae76e-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ae76e-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ae76e-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
