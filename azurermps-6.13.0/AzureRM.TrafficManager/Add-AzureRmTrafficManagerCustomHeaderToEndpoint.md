---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680293"
---
# <span data-ttu-id="b2111-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="b2111-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2111-102">SYNOPSIS</span></span>
<span data-ttu-id="b2111-103">Egyéni fejléc-információt ad hozzá egy helyi forgalomirányítási végpont-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b2111-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2111-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2111-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2111-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2111-105">DESCRIPTION</span></span>
<span data-ttu-id="b2111-106">Az **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** parancsmag az Egyéni fejléc-információkat hozzáadja egy helyi Azure Traffic Manager végpont-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b2111-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="b2111-107">Végpontot a New-AzureRmTrafficManagerEndpoint vagy Get-AzureRmTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="b2111-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="b2111-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="b2111-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="b2111-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzureRmTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b2111-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b2111-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b2111-110">EXAMPLES</span></span>

### <span data-ttu-id="b2111-111">Példa 1: Egyéni fejléc-információ hozzáadása egy végponthoz</span><span class="sxs-lookup"><span data-stu-id="b2111-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="b2111-112">Az első parancs az Azure Traffic Manager végpontját a **New-AzureRmTrafficManagerEndpoint** parancsmag segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b2111-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="b2111-113">A parancs a $TrafficManagerEndpoint változóban tárolja a helyi végpontot.</span><span class="sxs-lookup"><span data-stu-id="b2111-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="b2111-114">A második parancs az Egyéni fejléc-információkat hozzáadja a $TrafficManagerEndpointban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="b2111-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="b2111-115">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b2111-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="b2111-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2111-116">PARAMETERS</span></span>

### <span data-ttu-id="b2111-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2111-117">-DefaultProfile</span></span>
<span data-ttu-id="b2111-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2111-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2111-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2111-119">-Name</span></span>
<span data-ttu-id="b2111-120">A hozzáadni kívánt egyéni fejléc-adatok nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2111-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="b2111-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b2111-122">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2111-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="b2111-123">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="b2111-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b2111-124">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzureRmTrafficManagerEndpoint vagy New-AzureRmTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b2111-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="b2111-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="b2111-125">-Value</span></span>
<span data-ttu-id="b2111-126">A hozzáadni kívánt egyéni fejléc-adatok értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2111-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="b2111-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2111-127">-Confirm</span></span>
<span data-ttu-id="b2111-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2111-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2111-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2111-129">-WhatIf</span></span>
<span data-ttu-id="b2111-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2111-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2111-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2111-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2111-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2111-132">CommonParameters</span></span>
<span data-ttu-id="b2111-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2111-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2111-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2111-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2111-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2111-135">INPUTS</span></span>

### <span data-ttu-id="b2111-136">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="b2111-137">Ez a parancsmag egy **TrafficManagerEndpoint** -objektumot fogad erre a parancsmagra.</span><span class="sxs-lookup"><span data-stu-id="b2111-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="b2111-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2111-138">OUTPUTS</span></span>

### <span data-ttu-id="b2111-139">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="b2111-140">Ez a parancsmag egy módosított **TrafficManagerEndpoint** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="b2111-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="b2111-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2111-141">NOTES</span></span>

## <span data-ttu-id="b2111-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2111-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2111-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="b2111-144">Új – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b2111-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2111-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b2111-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2111-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
