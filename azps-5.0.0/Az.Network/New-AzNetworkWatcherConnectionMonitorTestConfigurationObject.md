---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302711"
---
# <span data-ttu-id="36575-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="36575-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="36575-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36575-102">SYNOPSIS</span></span>
<span data-ttu-id="36575-103">Kapcsolati monitor tesztelési konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="36575-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="36575-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36575-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36575-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36575-105">DESCRIPTION</span></span>
<span data-ttu-id="36575-106">Az New-AzNetworkWatcherConnectionMonitorTestConfigurationObject parancsmag létrehoz egy kapcsolat-monitor teszt-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36575-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="36575-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36575-107">EXAMPLES</span></span>

### <span data-ttu-id="36575-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36575-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="36575-109">Név: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "Method": "GET", "RequestHeaders": [{"név": "Allow", "value": "GET"}], "ValidStatusCodeRanges": ["2xx"; "300-308"]; "PreferHTTPS": true} SuccessThreshold: {"ChecksFailedPercent": 20, "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="36575-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="36575-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36575-110">PARAMETERS</span></span>

### <span data-ttu-id="36575-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36575-111">-DefaultProfile</span></span>
<span data-ttu-id="36575-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36575-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36575-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36575-113">-Name</span></span>
<span data-ttu-id="36575-114">A kapcsolat figyelője teszt-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="36575-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="36575-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="36575-115">-PreferredIPVersion</span></span>
<span data-ttu-id="36575-116">A tesztelés kiértékeléséhez használni kívánt IP-verzió.</span><span class="sxs-lookup"><span data-stu-id="36575-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="36575-117">Előfordulhat, hogy a kapcsolati monitor más paraméterektől függően eltérő verziót használ.</span><span class="sxs-lookup"><span data-stu-id="36575-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="36575-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="36575-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="36575-119">Az egyes protokollokon végzett tesztelési értékeléshez használt paraméterek.</span><span class="sxs-lookup"><span data-stu-id="36575-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36575-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="36575-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="36575-121">A teszteléshez csak a sikeres kiértékeléshez engedélyezett sikertelen vizsgálatok maximális százalékos aránya.</span><span class="sxs-lookup"><span data-stu-id="36575-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="36575-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="36575-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="36575-123">A vizsgálat során az eredményként való kiértékeléshez megengedett maximális idő ezredmásodpercben.</span><span class="sxs-lookup"><span data-stu-id="36575-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36575-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="36575-124">-TestFrequencySec</span></span>
<span data-ttu-id="36575-125">A teszt kiértékelésének gyakorisága másodpercben.</span><span class="sxs-lookup"><span data-stu-id="36575-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36575-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36575-126">-Confirm</span></span>
<span data-ttu-id="36575-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36575-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36575-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36575-128">-WhatIf</span></span>
<span data-ttu-id="36575-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36575-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36575-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36575-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36575-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36575-131">CommonParameters</span></span>
<span data-ttu-id="36575-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36575-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36575-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36575-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36575-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36575-134">INPUTS</span></span>

### <span data-ttu-id="36575-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="36575-135">None</span></span>

## <span data-ttu-id="36575-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36575-136">OUTPUTS</span></span>

### <span data-ttu-id="36575-137">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="36575-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="36575-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36575-138">NOTES</span></span>

## <span data-ttu-id="36575-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36575-139">RELATED LINKS</span></span>
