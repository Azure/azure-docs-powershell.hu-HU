---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014475"
---
# <span data-ttu-id="0c79c-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="0c79c-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="0c79c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c79c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c79c-103">Új társközi ASN-t hoz létre</span><span class="sxs-lookup"><span data-stu-id="0c79c-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="0c79c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c79c-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c79c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c79c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c79c-106">Új PeerAsn objektum létrehozása az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="0c79c-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="0c79c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c79c-107">EXAMPLES</span></span>

### <span data-ttu-id="0c79c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c79c-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="0c79c-109">Új PeerAsn létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c79c-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="0c79c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c79c-110">PARAMETERS</span></span>

### <span data-ttu-id="0c79c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c79c-111">-AsJob</span></span>
<span data-ttu-id="0c79c-112">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="0c79c-112">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c79c-113">-DefaultProfile</span></span>
<span data-ttu-id="0c79c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c79c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c79c-115">– E-mail</span><span class="sxs-lookup"><span data-stu-id="0c79c-115">-Email</span></span>
<span data-ttu-id="0c79c-116">E-mail</span><span class="sxs-lookup"><span data-stu-id="0c79c-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c79c-117">-Name</span></span>
<span data-ttu-id="0c79c-118">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="0c79c-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="0c79c-119">-PeerAsn</span></span>
<span data-ttu-id="0c79c-120">A társközi ASN-erőforrás azonosítója. az azonosító lekéréséhez használja a Get-AzPeerAsn.</span><span class="sxs-lookup"><span data-stu-id="0c79c-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="0c79c-121">-PeerName</span></span>
<span data-ttu-id="0c79c-122">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="0c79c-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="0c79c-123">-Phone</span></span>
<span data-ttu-id="0c79c-124">Phone</span><span class="sxs-lookup"><span data-stu-id="0c79c-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c79c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c79c-125">-Confirm</span></span>
<span data-ttu-id="0c79c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c79c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c79c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c79c-127">-WhatIf</span></span>
<span data-ttu-id="0c79c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c79c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c79c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c79c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c79c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c79c-130">CommonParameters</span></span>
<span data-ttu-id="0c79c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c79c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c79c-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c79c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c79c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c79c-133">INPUTS</span></span>

### <span data-ttu-id="0c79c-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="0c79c-134">None</span></span>

## <span data-ttu-id="0c79c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c79c-135">OUTPUTS</span></span>

### <span data-ttu-id="0c79c-136">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="0c79c-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="0c79c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c79c-137">NOTES</span></span>

## <span data-ttu-id="0c79c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c79c-138">RELATED LINKS</span></span>
