---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: af18a5a93cf08fe4806af429aee667b569c527d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680292"
---
# <span data-ttu-id="1b65c-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="1b65c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b65c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b65c-103">Eltávolítja az egyéni élőfej-információkat egy helyi forgalomirányítási profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="1b65c-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b65c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b65c-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromProfile -Name <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b65c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b65c-105">DESCRIPTION</span></span>
<span data-ttu-id="1b65c-106">A **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** parancsmag egy helyi Azure Traffic Manager-profil objektumból távolítja el az egyéni élőfej-információkat.</span><span class="sxs-lookup"><span data-stu-id="1b65c-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1b65c-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="1b65c-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="1b65c-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="1b65c-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1b65c-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="1b65c-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="1b65c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1b65c-110">EXAMPLES</span></span>

### <span data-ttu-id="1b65c-111">Példa 1: Egyéni fejléc-adatok eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="1b65c-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1b65c-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1b65c-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1b65c-113">A második parancs eltávolítja az Egyéni fejléc-információkat az $TrafficManagerProfile tárolt profilból.</span><span class="sxs-lookup"><span data-stu-id="1b65c-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1b65c-114">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="1b65c-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1b65c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b65c-115">PARAMETERS</span></span>

### <span data-ttu-id="1b65c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-116">-DefaultProfile</span></span>
<span data-ttu-id="1b65c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b65c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b65c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1b65c-118">-Name</span></span>
<span data-ttu-id="1b65c-119">Az eltávolítani kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b65c-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="1b65c-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="1b65c-121">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1b65c-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1b65c-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="1b65c-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1b65c-123">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b65c-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1b65c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b65c-124">-Confirm</span></span>
<span data-ttu-id="1b65c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b65c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b65c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b65c-126">-WhatIf</span></span>
<span data-ttu-id="1b65c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b65c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b65c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b65c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b65c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b65c-129">CommonParameters</span></span>
<span data-ttu-id="1b65c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b65c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b65c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b65c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b65c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b65c-132">INPUTS</span></span>

### <span data-ttu-id="1b65c-133">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1b65c-134">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="1b65c-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="1b65c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b65c-135">OUTPUTS</span></span>

### <span data-ttu-id="1b65c-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1b65c-137">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1b65c-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="1b65c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b65c-138">NOTES</span></span>

## <span data-ttu-id="1b65c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b65c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b65c-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="1b65c-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1b65c-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b65c-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
