---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492681"
---
# <span data-ttu-id="c2839-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="c2839-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2839-102">SYNOPSIS</span></span>
<span data-ttu-id="c2839-103">Eltávolítja az egyéni élőfej-információkat egy helyi forgalomirányítási végpont-objektumból.</span><span class="sxs-lookup"><span data-stu-id="c2839-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2839-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2839-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2839-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2839-105">DESCRIPTION</span></span>
<span data-ttu-id="c2839-106">A **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** parancsmag eltávolítja az egyéni élőfej-információkat egy helyi Azure Traffic Manager végpont-objektumból.</span><span class="sxs-lookup"><span data-stu-id="c2839-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="c2839-107">Végpontot a New-AzureRmTrafficManagerEndpoint vagy Get-AzureRmTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="c2839-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="c2839-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="c2839-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="c2839-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzureRmTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c2839-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="c2839-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c2839-110">EXAMPLES</span></span>

### <span data-ttu-id="c2839-111">Példa 1: egyéni alhálózati adatok eltávolítása végpontról</span><span class="sxs-lookup"><span data-stu-id="c2839-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="c2839-112">Az első parancs megkapja a contoso nevű Azure-végpontot a ContosoProfile nevű ResourceGroup11 nevű erőforráscsoport profiljában, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c2839-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="c2839-113">A második parancs eltávolítja az Egyéni fejléc-adatokat a $TrafficManagerEndpointban tárolt végpontból.</span><span class="sxs-lookup"><span data-stu-id="c2839-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c2839-114">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="c2839-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="c2839-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2839-115">PARAMETERS</span></span>

### <span data-ttu-id="c2839-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2839-116">-DefaultProfile</span></span>
<span data-ttu-id="c2839-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2839-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2839-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2839-118">-Name</span></span>
<span data-ttu-id="c2839-119">Az eltávolítani kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2839-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="c2839-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c2839-121">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c2839-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="c2839-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="c2839-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c2839-123">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzureRmTrafficManagerEndpoint vagy New-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2839-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2839-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2839-124">-Confirm</span></span>
<span data-ttu-id="c2839-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2839-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2839-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2839-126">-WhatIf</span></span>
<span data-ttu-id="c2839-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2839-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2839-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2839-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2839-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2839-129">CommonParameters</span></span>
<span data-ttu-id="c2839-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2839-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2839-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2839-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2839-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2839-132">INPUTS</span></span>

### <span data-ttu-id="c2839-133">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="c2839-134">Ez a parancsmag egy **TrafficManagerEndpoint** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="c2839-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="c2839-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2839-135">OUTPUTS</span></span>

### <span data-ttu-id="c2839-136">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="c2839-137">Ez a parancsmag egy módosított TrafficManagerEndpoint objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c2839-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="c2839-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2839-138">NOTES</span></span>

## <span data-ttu-id="c2839-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2839-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2839-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="c2839-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2839-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c2839-142">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c2839-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2839-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
