---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194152"
---
# <span data-ttu-id="6f05b-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="6f05b-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="6f05b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f05b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f05b-103">Címtartomány vagy alhálózat eltávolítása egy helyi forgalomirányítási végpont-objektumból.</span><span class="sxs-lookup"><span data-stu-id="6f05b-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="6f05b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f05b-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f05b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f05b-105">DESCRIPTION</span></span>
<span data-ttu-id="6f05b-106">A **Remove-AzTrafficManagerIpAddressRange** parancsmag a helyi Azure Traffic Manager végpont-objektumból távolítja el az IP-cím tartományát.</span><span class="sxs-lookup"><span data-stu-id="6f05b-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="6f05b-107">Végpontot a New-AzTrafficManagerEndpoint vagy Get-AzTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="6f05b-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="6f05b-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="6f05b-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="6f05b-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6f05b-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6f05b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f05b-110">EXAMPLES</span></span>

### <span data-ttu-id="6f05b-111">1. példa: az IP-címtartományok eltávolítása végpontról</span><span class="sxs-lookup"><span data-stu-id="6f05b-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="6f05b-112">Az első parancs megkapja a contoso nevű Azure-végpontot a ContosoProfile nevű ResourceGroup11 nevű erőforráscsoport profiljában, majd az adott objektumot a $TrafficManagerEndpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6f05b-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="6f05b-113">A második parancs eltávolítja az IP-címtartományt a $TrafficManagerEndpointban tárolt végpontból.</span><span class="sxs-lookup"><span data-stu-id="6f05b-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="6f05b-114">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="6f05b-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="6f05b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f05b-115">PARAMETERS</span></span>

### <span data-ttu-id="6f05b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f05b-116">-DefaultProfile</span></span>
<span data-ttu-id="6f05b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f05b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f05b-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f05b-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6f05b-119">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6f05b-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="6f05b-120">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="6f05b-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6f05b-121">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6f05b-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6f05b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f05b-122">-Confirm</span></span>
<span data-ttu-id="6f05b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f05b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f05b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f05b-124">-WhatIf</span></span>
<span data-ttu-id="6f05b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f05b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f05b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f05b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f05b-127">– Első</span><span class="sxs-lookup"><span data-stu-id="6f05b-127">-First</span></span>
<span data-ttu-id="6f05b-128">Az első IP-címet adja meg az eltávolítandó adattartománnyal.</span><span class="sxs-lookup"><span data-stu-id="6f05b-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="6f05b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f05b-129">CommonParameters</span></span>
<span data-ttu-id="6f05b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f05b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f05b-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f05b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f05b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f05b-132">INPUTS</span></span>

### <span data-ttu-id="6f05b-133">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f05b-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6f05b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f05b-134">OUTPUTS</span></span>

### <span data-ttu-id="6f05b-135">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f05b-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6f05b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f05b-136">NOTES</span></span>

## <span data-ttu-id="6f05b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f05b-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f05b-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="6f05b-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="6f05b-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f05b-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6f05b-140">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f05b-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6f05b-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f05b-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)