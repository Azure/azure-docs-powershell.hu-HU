---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194032"
---
# <span data-ttu-id="018d6-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="018d6-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="018d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="018d6-102">SYNOPSIS</span></span>
<span data-ttu-id="018d6-103">Nyilvános IP-telefonszámok a virtuális központi tűzfalon</span><span class="sxs-lookup"><span data-stu-id="018d6-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="018d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="018d6-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="018d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="018d6-105">DESCRIPTION</span></span>
<span data-ttu-id="018d6-106">Nyilvános IP-telefonszámok a virtuális központi tűzfalon</span><span class="sxs-lookup"><span data-stu-id="018d6-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="018d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="018d6-107">EXAMPLES</span></span>

### <span data-ttu-id="018d6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="018d6-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="018d6-109">Ez két nyilvános IP-t hoz létre a virtuális hub-hoz csatlakoztatott tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="018d6-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="018d6-110">Ekkor létrejön az IP-cím a háttérben. Új tűzfal esetében nem lehet explicit módon megadni az IP-ket.</span><span class="sxs-lookup"><span data-stu-id="018d6-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="018d6-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="018d6-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="018d6-112">Ezzel létrehoz egy új nyilvános IP-t a tűzfalon, és megtartja $publicIp 1, $publicIp 2, amely már megtalálható a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="018d6-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="018d6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="018d6-113">PARAMETERS</span></span>

### <span data-ttu-id="018d6-114">-Címek</span><span class="sxs-lookup"><span data-stu-id="018d6-114">-Addresses</span></span>
<span data-ttu-id="018d6-115">A hub-hoz csatlakoztatott tűzfal nyilvános IP-címei</span><span class="sxs-lookup"><span data-stu-id="018d6-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018d6-116">-Count</span><span class="sxs-lookup"><span data-stu-id="018d6-116">-Count</span></span>
<span data-ttu-id="018d6-117">Nyilvános IP-címek száma</span><span class="sxs-lookup"><span data-stu-id="018d6-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018d6-118">-DefaultProfile</span></span>
<span data-ttu-id="018d6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="018d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018d6-120">CommonParameters</span></span>
<span data-ttu-id="018d6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="018d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018d6-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="018d6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018d6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="018d6-123">INPUTS</span></span>

### <span data-ttu-id="018d6-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="018d6-124">None</span></span>

## <span data-ttu-id="018d6-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="018d6-125">OUTPUTS</span></span>

### <span data-ttu-id="018d6-126">Microsoft. Azure. commands. Network. models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="018d6-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="018d6-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="018d6-127">NOTES</span></span>

## <span data-ttu-id="018d6-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="018d6-128">RELATED LINKS</span></span>
