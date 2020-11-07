---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841565"
---
# <span data-ttu-id="95339-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="95339-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="95339-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95339-102">SYNOPSIS</span></span>
<span data-ttu-id="95339-103">Az összes elérhető internetszolgáltató felsorolása egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="95339-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="95339-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95339-104">SYNTAX</span></span>

### <span data-ttu-id="95339-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95339-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95339-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="95339-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95339-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="95339-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95339-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="95339-108">DESCRIPTION</span></span>
<span data-ttu-id="95339-109">A Get-AzNetworkWatcherReachabilityProvidersList felsorolja az összes elérhető internetszolgáltatót egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="95339-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="95339-110">Példák</span><span class="sxs-lookup"><span data-stu-id="95339-110">EXAMPLES</span></span>

### <span data-ttu-id="95339-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="95339-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="95339-112">Felsorolja az összes elérhető szolgáltatót a Seattle-i, az Azure Data Center in West US-ben.</span><span class="sxs-lookup"><span data-stu-id="95339-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="95339-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95339-113">PARAMETERS</span></span>

### <span data-ttu-id="95339-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95339-114">-AsJob</span></span>
<span data-ttu-id="95339-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="95339-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-116">-Város</span><span class="sxs-lookup"><span data-stu-id="95339-116">-City</span></span>
<span data-ttu-id="95339-117">A város neve.</span><span class="sxs-lookup"><span data-stu-id="95339-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-118">-Ország</span><span class="sxs-lookup"><span data-stu-id="95339-118">-Country</span></span>
<span data-ttu-id="95339-119">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="95339-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95339-120">-DefaultProfile</span></span>
<span data-ttu-id="95339-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95339-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="95339-122">-Location</span></span>
<span data-ttu-id="95339-123">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="95339-123">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95339-124">-NetworkWatcher</span></span>
<span data-ttu-id="95339-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="95339-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95339-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="95339-126">-NetworkWatcherName</span></span>
<span data-ttu-id="95339-127">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="95339-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95339-128">-ResourceGroupName</span></span>
<span data-ttu-id="95339-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="95339-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95339-130">-ResourceId</span></span>
<span data-ttu-id="95339-131">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="95339-131">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95339-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="95339-132">-State</span></span>
<span data-ttu-id="95339-133">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="95339-133">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95339-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95339-134">CommonParameters</span></span>
<span data-ttu-id="95339-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95339-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95339-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95339-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95339-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95339-137">INPUTS</span></span>

### <span data-ttu-id="95339-138">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95339-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="95339-139">System. String System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="95339-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="95339-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95339-140">OUTPUTS</span></span>

### <span data-ttu-id="95339-141">Microsoft. Azure. commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="95339-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="95339-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95339-142">NOTES</span></span>
<span data-ttu-id="95339-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="95339-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="95339-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95339-144">RELATED LINKS</span></span>

[<span data-ttu-id="95339-145">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95339-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="95339-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95339-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="95339-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="95339-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="95339-148">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="95339-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="95339-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="95339-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="95339-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="95339-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="95339-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="95339-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="95339-152">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95339-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95339-153">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="95339-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="95339-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95339-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95339-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95339-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="95339-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95339-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
