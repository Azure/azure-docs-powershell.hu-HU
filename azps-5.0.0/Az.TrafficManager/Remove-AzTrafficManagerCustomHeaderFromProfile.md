---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186378"
---
# <span data-ttu-id="9836c-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="9836c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9836c-102">SYNOPSIS</span></span>
<span data-ttu-id="9836c-103">Eltávolítja az egyéni élőfej-információkat egy helyi forgalomirányítási profil objektumból.</span><span class="sxs-lookup"><span data-stu-id="9836c-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="9836c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9836c-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9836c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9836c-105">DESCRIPTION</span></span>
<span data-ttu-id="9836c-106">A **Remove-AzTrafficManagerCustomHeaderFromProfile** parancsmag egy helyi Azure Traffic Manager-profil objektumból távolítja el az egyéni élőfej-információkat.</span><span class="sxs-lookup"><span data-stu-id="9836c-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9836c-107">A New-AzTrafficManagerProfile-vagy Get-AzTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="9836c-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9836c-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="9836c-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9836c-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="9836c-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9836c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9836c-110">EXAMPLES</span></span>

### <span data-ttu-id="9836c-111">Példa 1: Egyéni fejléc-adatok eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="9836c-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9836c-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9836c-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9836c-113">A második parancs eltávolítja az Egyéni fejléc-információkat az $TrafficManagerProfile tárolt profilból.</span><span class="sxs-lookup"><span data-stu-id="9836c-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9836c-114">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="9836c-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9836c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9836c-115">PARAMETERS</span></span>

### <span data-ttu-id="9836c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-116">-DefaultProfile</span></span>
<span data-ttu-id="9836c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9836c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9836c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9836c-118">-Name</span></span>
<span data-ttu-id="9836c-119">Az eltávolítani kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9836c-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="9836c-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="9836c-121">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9836c-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9836c-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="9836c-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9836c-123">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9836c-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9836c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9836c-124">-Confirm</span></span>
<span data-ttu-id="9836c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9836c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9836c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9836c-126">-WhatIf</span></span>
<span data-ttu-id="9836c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9836c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9836c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9836c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9836c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9836c-129">CommonParameters</span></span>
<span data-ttu-id="9836c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9836c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9836c-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9836c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9836c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9836c-132">INPUTS</span></span>

### <span data-ttu-id="9836c-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9836c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9836c-134">OUTPUTS</span></span>

### <span data-ttu-id="9836c-135">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9836c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9836c-136">NOTES</span></span>

## <span data-ttu-id="9836c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9836c-137">RELATED LINKS</span></span>

[<span data-ttu-id="9836c-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="9836c-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9836c-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9836c-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)