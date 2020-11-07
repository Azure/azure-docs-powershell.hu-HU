---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668423"
---
# <span data-ttu-id="52dc1-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="52dc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="52dc1-103">Egyéni fejléc-információt ad hozzá egy helyi forgalomirányítási végpont-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="52dc1-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="52dc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52dc1-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52dc1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="52dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="52dc1-106">Az **Add-AzTrafficManagerCustomHeaderToEndpoint** parancsmag az Egyéni fejléc-információkat hozzáadja egy helyi Azure Traffic Manager végpont-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="52dc1-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="52dc1-107">Végpontot a New-AzTrafficManagerEndpoint vagy Get-AzTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="52dc1-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="52dc1-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="52dc1-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="52dc1-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="52dc1-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="52dc1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52dc1-110">EXAMPLES</span></span>

### <span data-ttu-id="52dc1-111">Példa 1: Egyéni fejléc-információ hozzáadása egy végponthoz</span><span class="sxs-lookup"><span data-stu-id="52dc1-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="52dc1-112">Az első parancs az Azure Traffic Manager végpontját a **New-AzTrafficManagerEndpoint** parancsmag segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="52dc1-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="52dc1-113">A parancs a $TrafficManagerEndpoint változóban tárolja a helyi végpontot.</span><span class="sxs-lookup"><span data-stu-id="52dc1-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="52dc1-114">A második parancs az Egyéni fejléc-információkat hozzáadja a $TrafficManagerEndpointban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="52dc1-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="52dc1-115">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="52dc1-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="52dc1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52dc1-116">PARAMETERS</span></span>

### <span data-ttu-id="52dc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52dc1-117">-DefaultProfile</span></span>
<span data-ttu-id="52dc1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52dc1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52dc1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52dc1-119">-Name</span></span>
<span data-ttu-id="52dc1-120">A hozzáadni kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52dc1-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="52dc1-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="52dc1-122">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="52dc1-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="52dc1-123">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="52dc1-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="52dc1-124">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="52dc1-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="52dc1-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="52dc1-125">-Value</span></span>
<span data-ttu-id="52dc1-126">A hozzáadni kívánt egyéni fejléc-adatok értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52dc1-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="52dc1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52dc1-127">-Confirm</span></span>
<span data-ttu-id="52dc1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52dc1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52dc1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52dc1-129">-WhatIf</span></span>
<span data-ttu-id="52dc1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52dc1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52dc1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52dc1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52dc1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52dc1-132">CommonParameters</span></span>
<span data-ttu-id="52dc1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52dc1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52dc1-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52dc1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52dc1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52dc1-135">INPUTS</span></span>

### <span data-ttu-id="52dc1-136">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="52dc1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52dc1-137">OUTPUTS</span></span>

### <span data-ttu-id="52dc1-138">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="52dc1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52dc1-139">NOTES</span></span>

## <span data-ttu-id="52dc1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52dc1-140">RELATED LINKS</span></span>

[<span data-ttu-id="52dc1-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="52dc1-142">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="52dc1-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="52dc1-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="52dc1-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52dc1-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
