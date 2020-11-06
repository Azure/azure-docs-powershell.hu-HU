---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491827"
---
# <span data-ttu-id="3657e-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3657e-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="3657e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3657e-102">SYNOPSIS</span></span>
<span data-ttu-id="3657e-103">A helyi forgalmi igazgató profil objektumhoz hozzáadja a várható állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="3657e-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3657e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3657e-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3657e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3657e-105">DESCRIPTION</span></span>
<span data-ttu-id="3657e-106">Az **Add-AzureRmTrafficManagerExpectedStatusCodeRange** parancsmag egy, a helyi Azure Traffic Manager-profil objektumba felvett, a várt állapotkódok tartományát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3657e-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3657e-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="3657e-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="3657e-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="3657e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3657e-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3657e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3657e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3657e-110">EXAMPLES</span></span>

### <span data-ttu-id="3657e-111">1. példa: a várt állapotkódot tartalmazó tartományok felvétele a profilba</span><span class="sxs-lookup"><span data-stu-id="3657e-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3657e-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3657e-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3657e-113">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="3657e-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="3657e-114">A második parancs hozzáadja a várt állapotkódot az $TrafficManagerProfile tárolt profilhoz.</span><span class="sxs-lookup"><span data-stu-id="3657e-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3657e-115">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="3657e-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3657e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3657e-116">PARAMETERS</span></span>

### <span data-ttu-id="3657e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-117">-DefaultProfile</span></span>
<span data-ttu-id="3657e-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3657e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3657e-119">-Max</span><span class="sxs-lookup"><span data-stu-id="3657e-119">-Max</span></span>
<span data-ttu-id="3657e-120">A felvenni kívánt állapotkód-intervallum legmagasabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3657e-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="3657e-121">-Min</span><span class="sxs-lookup"><span data-stu-id="3657e-121">-Min</span></span>
<span data-ttu-id="3657e-122">A hozzáadandó állapotkód-tartományok legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3657e-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="3657e-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="3657e-124">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3657e-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3657e-125">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="3657e-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3657e-126">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3657e-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3657e-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3657e-127">-Confirm</span></span>
<span data-ttu-id="3657e-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3657e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3657e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3657e-129">-WhatIf</span></span>
<span data-ttu-id="3657e-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3657e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3657e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3657e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3657e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3657e-132">CommonParameters</span></span>
<span data-ttu-id="3657e-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3657e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3657e-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3657e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3657e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3657e-135">INPUTS</span></span>

### <span data-ttu-id="3657e-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3657e-137">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="3657e-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="3657e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3657e-138">OUTPUTS</span></span>

### <span data-ttu-id="3657e-139">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3657e-140">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3657e-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="3657e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3657e-141">NOTES</span></span>

## <span data-ttu-id="3657e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3657e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3657e-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3657e-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="3657e-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3657e-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3657e-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
