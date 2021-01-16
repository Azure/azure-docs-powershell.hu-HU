---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334925"
---
# <span data-ttu-id="1da90-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1da90-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="1da90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da90-102">SYNOPSIS</span></span>
<span data-ttu-id="1da90-103">Nyilvános ip assoicated to the firewall on virtual hub</span><span class="sxs-lookup"><span data-stu-id="1da90-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="1da90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1da90-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da90-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1da90-105">DESCRIPTION</span></span>
<span data-ttu-id="1da90-106">Nyilvános ip assoicated to the firewall on virtual hub</span><span class="sxs-lookup"><span data-stu-id="1da90-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="1da90-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1da90-107">EXAMPLES</span></span>

### <span data-ttu-id="1da90-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1da90-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="1da90-109">Ezzel 2 nyilvános ip-címet hoz létre a virtuális központhoz csatlakoztatott tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="1da90-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="1da90-110">Ezzel létrehozza az IP-címet a háttérben. Az ipaddresseseket nem tudjuk kifejezetten biztosítani az új tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="1da90-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="1da90-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="1da90-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="1da90-112">Ezzel 1 új nyilvános ip-címet hoz létre a tűzfalon a $publicIp 1, $publicIp 2, amelyek már léteznek a tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="1da90-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="1da90-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1da90-113">PARAMETERS</span></span>

### <span data-ttu-id="1da90-114">-Címek</span><span class="sxs-lookup"><span data-stu-id="1da90-114">-Addresses</span></span>
<span data-ttu-id="1da90-115">A központi tűzfal nyilvános IP-címei</span><span class="sxs-lookup"><span data-stu-id="1da90-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="1da90-116">-Count</span><span class="sxs-lookup"><span data-stu-id="1da90-116">-Count</span></span>
<span data-ttu-id="1da90-117">A nyilvános IP-címek száma</span><span class="sxs-lookup"><span data-stu-id="1da90-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="1da90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da90-118">-DefaultProfile</span></span>
<span data-ttu-id="1da90-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1da90-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1da90-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da90-120">CommonParameters</span></span>
<span data-ttu-id="1da90-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da90-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da90-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1da90-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da90-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1da90-123">INPUTS</span></span>

### <span data-ttu-id="1da90-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="1da90-124">None</span></span>

## <span data-ttu-id="1da90-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1da90-125">OUTPUTS</span></span>

### <span data-ttu-id="1da90-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="1da90-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="1da90-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1da90-127">NOTES</span></span>

## <span data-ttu-id="1da90-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1da90-128">RELATED LINKS</span></span>
