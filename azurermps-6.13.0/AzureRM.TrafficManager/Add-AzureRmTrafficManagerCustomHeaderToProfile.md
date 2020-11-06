---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504236"
---
# <span data-ttu-id="fc0aa-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="fc0aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0aa-103">Egyéni fejléc-információt ad hozzá egy helyi forgalomirányítási profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc0aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc0aa-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc0aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc0aa-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0aa-106">Az **Add-AzureRmTrafficManagerCustomHeaderToProfile** parancsmag Egyéni fejléc-információkat ad hozzá egy helyi Azure Traffic Manager-profil objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-106">The **Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="fc0aa-107">A New-AzureRmTrafficManagerProfile-vagy Get-AzureRmTrafficManagerProfile-parancsmagok használatával is felveheti a profilt.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="fc0aa-108">Ez a parancsmag a helyi profil objektumon dolgozik.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="fc0aa-109">Végezze el a módosításokat a Traffic Manager profiljában a Set-AzureRmTrafficManagerProfile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fc0aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc0aa-110">EXAMPLES</span></span>

### <span data-ttu-id="fc0aa-111">Példa 1: Egyéni fejléc-információ hozzáadása egy profilhoz</span><span class="sxs-lookup"><span data-stu-id="fc0aa-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="fc0aa-112">Az első parancs az Azure Traffic Manager-profilt a **Get-AzureRmTrafficManagerProfile** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="fc0aa-113">A parancs a $TrafficManagerProfile változóban tárolja a helyi profilt.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="fc0aa-114">A második parancs hozzáadja az Egyéni fejléc-információkat az $TrafficManagerProfile tárolt profiljához.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="fc0aa-115">A végleges parancs a Traffic Managerben frissíti a profilt a $TrafficManagerProfile helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="fc0aa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc0aa-116">PARAMETERS</span></span>

### <span data-ttu-id="fc0aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-117">-DefaultProfile</span></span>
<span data-ttu-id="fc0aa-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0aa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc0aa-119">-Name</span></span>
<span data-ttu-id="fc0aa-120">A hozzáadni kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="fc0aa-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="fc0aa-122">Helyi **TrafficManagerProfile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fc0aa-123">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="fc0aa-124">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fc0aa-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="fc0aa-125">-Value</span></span>
<span data-ttu-id="fc0aa-126">A hozzáadni kívánt egyéni fejléc-adatok értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="fc0aa-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc0aa-127">-Confirm</span></span>
<span data-ttu-id="fc0aa-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0aa-129">-WhatIf</span></span>
<span data-ttu-id="fc0aa-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc0aa-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0aa-132">CommonParameters</span></span>
<span data-ttu-id="fc0aa-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc0aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0aa-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0aa-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc0aa-135">INPUTS</span></span>

### <span data-ttu-id="fc0aa-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="fc0aa-137">Ez a parancsmag egy **TrafficManagerProfile** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="fc0aa-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc0aa-138">OUTPUTS</span></span>

### <span data-ttu-id="fc0aa-139">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="fc0aa-140">Ez a parancsmag egy módosított **TrafficManagerProfile** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc0aa-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="fc0aa-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc0aa-141">NOTES</span></span>

## <span data-ttu-id="fc0aa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc0aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="fc0aa-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="fc0aa-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fc0aa-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc0aa-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
