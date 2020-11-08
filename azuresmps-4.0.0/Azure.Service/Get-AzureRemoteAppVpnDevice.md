---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015626"
---
# <span data-ttu-id="0265f-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="0265f-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="0265f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0265f-102">SYNOPSIS</span></span>
<span data-ttu-id="0265f-103">Információt keres a VPN-eszközökről.</span><span class="sxs-lookup"><span data-stu-id="0265f-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="0265f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0265f-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0265f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0265f-105">DESCRIPTION</span></span>
<span data-ttu-id="0265f-106">A **Get-AzureRemoteAppVpnDevice** parancsmag információt keres a virtuális MAGÁNHÁLÓZATI (VPN) eszközökről.</span><span class="sxs-lookup"><span data-stu-id="0265f-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="0265f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0265f-107">EXAMPLES</span></span>

### <span data-ttu-id="0265f-108">1. példa: az elérhető VPN-eszközök konfigurációjának visszaküldése virtuális hálózat számára</span><span class="sxs-lookup"><span data-stu-id="0265f-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="0265f-109">A parancs a megadott virtuális hálózat számára elérhető VPN-eszközök konfigurációját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0265f-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="0265f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0265f-110">PARAMETERS</span></span>

### <span data-ttu-id="0265f-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="0265f-111">-Profile</span></span>
<span data-ttu-id="0265f-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0265f-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0265f-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0265f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0265f-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="0265f-114">-VNetName</span></span>
<span data-ttu-id="0265f-115">Az Azure RemoteApp virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0265f-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0265f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0265f-116">CommonParameters</span></span>
<span data-ttu-id="0265f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0265f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0265f-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0265f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0265f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0265f-119">INPUTS</span></span>

## <span data-ttu-id="0265f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0265f-120">OUTPUTS</span></span>

### <span data-ttu-id="0265f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0265f-121">System.String</span></span>

## <span data-ttu-id="0265f-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0265f-122">NOTES</span></span>

## <span data-ttu-id="0265f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0265f-123">RELATED LINKS</span></span>

[<span data-ttu-id="0265f-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="0265f-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="0265f-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="0265f-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


