---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011018"
---
# <span data-ttu-id="d5d99-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d5d99-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="d5d99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5d99-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d99-103">A TCP-, HTTP-vagy ICMP-alapú teszt-értékeléshez használt protokoll-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d5d99-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="d5d99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5d99-104">SYNTAX</span></span>

### <span data-ttu-id="d5d99-105">TCP</span><span class="sxs-lookup"><span data-stu-id="d5d99-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d99-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="d5d99-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d99-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="d5d99-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d99-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5d99-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d99-109">A New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject parancsmag protokoll-konfigurációt hoz létre a TCP, a HTTP vagy az ICMP protokollal végzett teszteléshez.</span><span class="sxs-lookup"><span data-stu-id="d5d99-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="d5d99-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d5d99-110">EXAMPLES</span></span>

### <span data-ttu-id="d5d99-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5d99-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="d5d99-112">Port: 80 DisableTraceRoute: false</span><span class="sxs-lookup"><span data-stu-id="d5d99-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="d5d99-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5d99-113">PARAMETERS</span></span>

### <span data-ttu-id="d5d99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d99-114">-DefaultProfile</span></span>
<span data-ttu-id="d5d99-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5d99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d99-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="d5d99-116">-DisableTraceRoute</span></span>
<span data-ttu-id="d5d99-117">Az az érték, amely azt jelzi, hogy le kell-e tiltani az elérésiút-vizsgálatot a nyomkövetési útvonallal</span><span class="sxs-lookup"><span data-stu-id="d5d99-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="d5d99-118">-HttpProtocol</span></span>
<span data-ttu-id="d5d99-119">HTTP-protokoll kapcsolója</span><span class="sxs-lookup"><span data-stu-id="d5d99-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="d5d99-120">-IcmpProtocol</span></span>
<span data-ttu-id="d5d99-121">ICMP-protokoll kapcsolója</span><span class="sxs-lookup"><span data-stu-id="d5d99-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-122">-Módszer</span><span class="sxs-lookup"><span data-stu-id="d5d99-122">-Method</span></span>
<span data-ttu-id="d5d99-123">A használandó HTTP-módszer.</span><span class="sxs-lookup"><span data-stu-id="d5d99-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-124">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d5d99-124">-Path</span></span>
<span data-ttu-id="d5d99-125">Az URI elérési útvonal-összetevője</span><span class="sxs-lookup"><span data-stu-id="d5d99-125">The path component of the URI.</span></span> <span data-ttu-id="d5d99-126">Például a \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="d5d99-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-127">-Port</span><span class="sxs-lookup"><span data-stu-id="d5d99-127">-Port</span></span>
<span data-ttu-id="d5d99-128">Annak a portnak a csatlakoztatása, amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="d5d99-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="d5d99-129">-PreferHTTPS</span></span>
<span data-ttu-id="d5d99-130">Az az érték, amely azt jelzi, hogy a HTTPS a HTTP-t részesíti előnyben olyan esetekben, ahol a választás nem explicit.</span><span class="sxs-lookup"><span data-stu-id="d5d99-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="d5d99-131">-RequestHeader</span></span>
<span data-ttu-id="d5d99-132">A kéréssel továbbítani kívánt HTTP-fejlécek.</span><span class="sxs-lookup"><span data-stu-id="d5d99-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="d5d99-133">-TcpProtocol</span></span>
<span data-ttu-id="d5d99-134">TCP-protokoll kapcsolója</span><span class="sxs-lookup"><span data-stu-id="d5d99-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="d5d99-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="d5d99-136">A sikeresnek ítélt HTTP-állapotkódok</span><span class="sxs-lookup"><span data-stu-id="d5d99-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="d5d99-137">Például \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="d5d99-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d99-138">CommonParameters</span></span>
<span data-ttu-id="d5d99-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5d99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d99-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5d99-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d99-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5d99-141">INPUTS</span></span>

### <span data-ttu-id="d5d99-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5d99-142">None</span></span>

## <span data-ttu-id="d5d99-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5d99-143">OUTPUTS</span></span>

### <span data-ttu-id="d5d99-144">Microsoft. Azure. commands. Network. models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d99-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="d5d99-145">Microsoft. Azure. commands. Network. models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d99-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="d5d99-146">Microsoft. Azure. commands. Network. models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5d99-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="d5d99-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5d99-147">NOTES</span></span>

## <span data-ttu-id="d5d99-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5d99-148">RELATED LINKS</span></span>
