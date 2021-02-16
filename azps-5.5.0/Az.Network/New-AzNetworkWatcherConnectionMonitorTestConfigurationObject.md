---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202763"
---
# <span data-ttu-id="45033-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="45033-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="45033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45033-102">SYNOPSIS</span></span>
<span data-ttu-id="45033-103">Kapcsolatfigyelő tesztkonfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="45033-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="45033-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45033-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45033-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45033-105">DESCRIPTION</span></span>
<span data-ttu-id="45033-106">A New-AzNetworkWatcherConnectionMonitorTestConfigurationObject parancsmag létrehoz egy kapcsolatfigyelő tesztkonfigurációt.</span><span class="sxs-lookup"><span data-stu-id="45033-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="45033-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45033-107">EXAMPLES</span></span>

### <span data-ttu-id="45033-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="45033-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="45033-109">Név: httpTC TestFrequencySec : 120 PreferredIPVersion: ProtocolConfiguration : { "Port": 443, "Módszer": "GET", "RequestHeaders": [ { "Name": "Allow"; "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="45033-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="45033-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45033-110">PARAMETERS</span></span>

### <span data-ttu-id="45033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45033-111">-DefaultProfile</span></span>
<span data-ttu-id="45033-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45033-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45033-113">-Name</span><span class="sxs-lookup"><span data-stu-id="45033-113">-Name</span></span>
<span data-ttu-id="45033-114">A kapcsolatfigyelő tesztkonfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="45033-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="45033-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="45033-115">-PreferredIPVersion</span></span>
<span data-ttu-id="45033-116">A teszt kiértékelése során használni kívánt IP-verzió.</span><span class="sxs-lookup"><span data-stu-id="45033-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="45033-117">A kapcsolatfigyelő más paraméterektől függően másik verziót is használhat.</span><span class="sxs-lookup"><span data-stu-id="45033-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="45033-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="45033-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="45033-119">Az egyes protokollok tesztelésének elvégzéséhez használt paraméterek.</span><span class="sxs-lookup"><span data-stu-id="45033-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="45033-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="45033-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="45033-121">A sikertelen vizsgálatok maximális százalékos értéke a sikeresként értékelhető teszthez.</span><span class="sxs-lookup"><span data-stu-id="45033-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="45033-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="45033-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="45033-123">A teszt sikeres kiértékeléséhez megengedett maximális oda-vissza menetidő ezredmásodpercben.</span><span class="sxs-lookup"><span data-stu-id="45033-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="45033-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="45033-124">-TestFrequencySec</span></span>
<span data-ttu-id="45033-125">A teszt kiértékelési gyakorisága másodpercben.</span><span class="sxs-lookup"><span data-stu-id="45033-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="45033-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45033-126">-Confirm</span></span>
<span data-ttu-id="45033-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="45033-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45033-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45033-128">-WhatIf</span></span>
<span data-ttu-id="45033-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="45033-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45033-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45033-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45033-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45033-131">CommonParameters</span></span>
<span data-ttu-id="45033-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45033-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45033-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45033-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45033-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45033-134">INPUTS</span></span>

### <span data-ttu-id="45033-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="45033-135">None</span></span>

## <span data-ttu-id="45033-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45033-136">OUTPUTS</span></span>

### <span data-ttu-id="45033-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="45033-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="45033-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45033-138">NOTES</span></span>

## <span data-ttu-id="45033-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45033-139">RELATED LINKS</span></span>
