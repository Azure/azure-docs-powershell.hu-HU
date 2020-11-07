---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845369"
---
# <span data-ttu-id="581ca-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="581ca-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="581ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="581ca-102">SYNOPSIS</span></span>
<span data-ttu-id="581ca-103">Címtartomány vagy alhálózat felvétele a helyi forgalomirányítási végpont-objektumba.</span><span class="sxs-lookup"><span data-stu-id="581ca-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="581ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="581ca-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="581ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="581ca-105">DESCRIPTION</span></span>
<span data-ttu-id="581ca-106">A **Add-AzTrafficManagerIpAddressRange** parancsmag IP-címtartományt ad egy helyi Azure Traffic Manager végpont objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="581ca-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="581ca-107">Végpontot a New-AzTrafficManagerEndpoint vagy Get-AzTrafficManagerEndpoint parancsmagok használatával kaphat.</span><span class="sxs-lookup"><span data-stu-id="581ca-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="581ca-108">Ez a parancsmag a helyi végpont-objektumon működik.</span><span class="sxs-lookup"><span data-stu-id="581ca-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="581ca-109">Végezze el a módosításokat a forgalomirányító végpontján a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="581ca-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="581ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="581ca-110">EXAMPLES</span></span>

### <span data-ttu-id="581ca-111">1. példa: IP-címtartományok felvétele a végpontba</span><span class="sxs-lookup"><span data-stu-id="581ca-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="581ca-112">Az első parancs az Azure Traffic Manager végpontját a **New-AzTrafficManagerEndpoint** parancsmag segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="581ca-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="581ca-113">A parancs a $TrafficManagerEndpoint változóban tárolja a helyi végpontot.</span><span class="sxs-lookup"><span data-stu-id="581ca-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="581ca-114">A második parancs hozzáadja az IP-címtartomány 1.2.3.4 a 5.6.7.8 $TrafficManagerEndpoint-ban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="581ca-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="581ca-115">A harmadik parancs hozzáadja az IP-címtartomány 9.10.11.0 a 9.10.11.255 $TrafficManagerEndpoint-ban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="581ca-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="581ca-116">A negyedik parancs ellenőrzi, hogy a hatókör megfelel-e a tartomány méretének, majd hozzáadja az IP-cím tartomány 12.13.14.0 a 12.13.14.31-$TrafficManagerEndpoint ban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="581ca-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="581ca-117">Az ötödik parancs hozzáadja az IP-címtartomány 15.16.17.18 a 15.16.17.18 $TrafficManagerEndpoint-ban tárolt végponthoz.</span><span class="sxs-lookup"><span data-stu-id="581ca-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="581ca-118">A végleges parancs a Traffic Manager végpontját frissíti a $TrafficManagerEndpoint helyi értékének megfelelően.</span><span class="sxs-lookup"><span data-stu-id="581ca-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="581ca-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="581ca-119">PARAMETERS</span></span>

### <span data-ttu-id="581ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581ca-120">-DefaultProfile</span></span>
<span data-ttu-id="581ca-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="581ca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="581ca-122">-Last</span><span class="sxs-lookup"><span data-stu-id="581ca-122">-Last</span></span>
<span data-ttu-id="581ca-123">A hozzáadni kívánt adattartománnyal utoljára megadott IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="581ca-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581ca-124">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="581ca-124">-Scope</span></span>
<span data-ttu-id="581ca-125">A hozzáadni kívánt IP-címtartomány tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="581ca-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581ca-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="581ca-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="581ca-127">Helyi **TrafficManagerEndpoint** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="581ca-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="581ca-128">Ez a parancsmag módosította ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="581ca-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="581ca-129">**TrafficManagerEndpoint** -objektum beolvasásához használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="581ca-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="581ca-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="581ca-130">-Confirm</span></span>
<span data-ttu-id="581ca-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="581ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="581ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581ca-132">-WhatIf</span></span>
<span data-ttu-id="581ca-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="581ca-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="581ca-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="581ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="581ca-135">– Első</span><span class="sxs-lookup"><span data-stu-id="581ca-135">-First</span></span>
<span data-ttu-id="581ca-136">A hozzáadni kívánt adattartománnyal az első IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="581ca-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="581ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581ca-137">CommonParameters</span></span>
<span data-ttu-id="581ca-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="581ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581ca-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581ca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581ca-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="581ca-140">INPUTS</span></span>

### <span data-ttu-id="581ca-141">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="581ca-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="581ca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="581ca-142">OUTPUTS</span></span>

### <span data-ttu-id="581ca-143">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="581ca-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="581ca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="581ca-144">NOTES</span></span>

## <span data-ttu-id="581ca-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="581ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="581ca-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="581ca-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="581ca-147">Új – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="581ca-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="581ca-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="581ca-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="581ca-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="581ca-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
