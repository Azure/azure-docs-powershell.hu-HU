---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011654"
---
# <span data-ttu-id="8235a-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="8235a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8235a-102">SYNOPSIS</span></span>
<span data-ttu-id="8235a-103">Egyéni fejléc-információt ad hozzá egy helyi forgalomirányítási profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8235a-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="8235a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8235a-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8235a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8235a-105">DESCRIPTION</span></span>
<span data-ttu-id="8235a-106">Az **Add-AzTrafficManagerCustomHeaderToProfile** parancsmag Egyéni fejléc-információkat ad hozzá egy helyi Azure Traffic Manager-profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8235a-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="8235a-107">A New-AzTrafficManagerProfile-vagy Get-AzTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="8235a-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="8235a-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8235a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="8235a-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8235a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="8235a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8235a-110">EXAMPLES</span></span>

### <span data-ttu-id="8235a-111">Példa 1: Egyéni fejléc-információ hozzáadása egy profilhoz</span><span class="sxs-lookup"><span data-stu-id="8235a-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="8235a-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8235a-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="8235a-113">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="8235a-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="8235a-114">A második parancs hozzáadja az Egyéni fejléc-információkat az $TrafficManagerProfile tárolt profiljához.</span><span class="sxs-lookup"><span data-stu-id="8235a-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="8235a-115">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="8235a-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="8235a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8235a-116">PARAMETERS</span></span>

### <span data-ttu-id="8235a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-117">-DefaultProfile</span></span>
<span data-ttu-id="8235a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8235a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8235a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8235a-119">-Name</span></span>
<span data-ttu-id="8235a-120">A hozzáadni kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8235a-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8235a-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="8235a-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8235a-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="8235a-123">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="8235a-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8235a-124">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8235a-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8235a-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="8235a-125">-Value</span></span>
<span data-ttu-id="8235a-126">A hozzáadni kívánt egyéni fejléc-adatok értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8235a-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8235a-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8235a-127">-Confirm</span></span>
<span data-ttu-id="8235a-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8235a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8235a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8235a-129">-WhatIf</span></span>
<span data-ttu-id="8235a-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8235a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8235a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8235a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8235a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8235a-132">CommonParameters</span></span>
<span data-ttu-id="8235a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8235a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8235a-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8235a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8235a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8235a-135">INPUTS</span></span>

### <span data-ttu-id="8235a-136">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8235a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8235a-137">OUTPUTS</span></span>

### <span data-ttu-id="8235a-138">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8235a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8235a-139">NOTES</span></span>

## <span data-ttu-id="8235a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8235a-140">RELATED LINKS</span></span>

[<span data-ttu-id="8235a-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="8235a-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8235a-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8235a-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
