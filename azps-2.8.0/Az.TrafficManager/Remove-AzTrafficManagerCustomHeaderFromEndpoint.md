---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f1575de761180c6ce17bcd6af1186d3e5bff60ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839933"
---
# <span data-ttu-id="e080a-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="e080a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e080a-102">SYNOPSIS</span></span>
<span data-ttu-id="e080a-103">Eltávolítja az egyéni élőfej-információkat egy helyi forgalomirányítási végpont-objektumból.</span><span class="sxs-lookup"><span data-stu-id="e080a-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="e080a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e080a-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e080a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e080a-105">DESCRIPTION</span></span>
<span data-ttu-id="e080a-106">A **Remove-AzTrafficManagerCustomHeaderFromEndpoint** parancsmag eltávolítja az egyéni élőfej-információkat egy helyi Azure Traffic Manager végpont-objektumból.</span><span class="sxs-lookup"><span data-stu-id="e080a-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e080a-107">Végpontot a New-AzTrafficManagerEndpoint vagy Get-AzTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="e080a-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e080a-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="e080a-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e080a-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e080a-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e080a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e080a-110">EXAMPLES</span></span>

### <span data-ttu-id="e080a-111">Példa 1: egyéni alhálózati adatok eltávolítása végpontról</span><span class="sxs-lookup"><span data-stu-id="e080a-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e080a-112">Az első parancs megkapja a contoso nevű Azure-végpontot a ContosoProfile nevű ResourceGroup11 nevű erőforráscsoport profiljában, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e080a-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e080a-113">A második parancs eltávolítja az Egyéni fejléc-adatokat a $TrafficManagerEndpointban tárolt végpontból.</span><span class="sxs-lookup"><span data-stu-id="e080a-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e080a-114">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e080a-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e080a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e080a-115">PARAMETERS</span></span>

### <span data-ttu-id="e080a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e080a-116">-DefaultProfile</span></span>
<span data-ttu-id="e080a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e080a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e080a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e080a-118">-Name</span></span>
<span data-ttu-id="e080a-119">Az eltávolítani kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e080a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="e080a-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e080a-121">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e080a-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e080a-122">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="e080a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e080a-123">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e080a-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e080a-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e080a-124">-Confirm</span></span>
<span data-ttu-id="e080a-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e080a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e080a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e080a-126">-WhatIf</span></span>
<span data-ttu-id="e080a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e080a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e080a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e080a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e080a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e080a-129">CommonParameters</span></span>
<span data-ttu-id="e080a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e080a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e080a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e080a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e080a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e080a-132">INPUTS</span></span>

### <span data-ttu-id="e080a-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e080a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e080a-134">OUTPUTS</span></span>

### <span data-ttu-id="e080a-135">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e080a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e080a-136">NOTES</span></span>

## <span data-ttu-id="e080a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e080a-137">RELATED LINKS</span></span>

[<span data-ttu-id="e080a-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="e080a-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e080a-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e080a-140">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e080a-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e080a-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
