---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 7931b993ff8374a84b0c2e963b8d615ce7a252fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847130"
---
# <span data-ttu-id="7d3ec-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7d3ec-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="7d3ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3ec-103">Elérhetőségi adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="7d3ec-103">Update Contact Information</span></span>

## <span data-ttu-id="7d3ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d3ec-104">SYNTAX</span></span>

### <span data-ttu-id="7d3ec-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d3ec-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3ec-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="7d3ec-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d3ec-107">DESCRIPTION</span></span>
<span data-ttu-id="7d3ec-108">Lehetővé teszi, hogy az előfizetésben szereplő PeerAsn frissítse a partnerek adatait.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="7d3ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d3ec-109">EXAMPLES</span></span>

### <span data-ttu-id="7d3ec-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d3ec-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="7d3ec-111">E-mail-cím hozzáadása a társközi ASN-hoz</span><span class="sxs-lookup"><span data-stu-id="7d3ec-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="7d3ec-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d3ec-112">PARAMETERS</span></span>

### <span data-ttu-id="7d3ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d3ec-113">-AsJob</span></span>
<span data-ttu-id="7d3ec-114">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-114">Run in the background.</span></span>

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

### <span data-ttu-id="7d3ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3ec-115">-DefaultProfile</span></span>
<span data-ttu-id="7d3ec-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d3ec-117">– E-mail</span><span class="sxs-lookup"><span data-stu-id="7d3ec-117">-Email</span></span>
<span data-ttu-id="7d3ec-118">E-mail</span><span class="sxs-lookup"><span data-stu-id="7d3ec-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3ec-119">-InputObject</span></span>
<span data-ttu-id="7d3ec-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="7d3ec-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3ec-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d3ec-121">-Name</span></span>
<span data-ttu-id="7d3ec-122">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3ec-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="7d3ec-123">-Phone</span></span>
<span data-ttu-id="7d3ec-124">Phone</span><span class="sxs-lookup"><span data-stu-id="7d3ec-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3ec-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d3ec-125">-Confirm</span></span>
<span data-ttu-id="7d3ec-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3ec-127">-WhatIf</span></span>
<span data-ttu-id="7d3ec-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d3ec-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d3ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3ec-130">CommonParameters</span></span>
<span data-ttu-id="7d3ec-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d3ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3ec-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3ec-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d3ec-133">INPUTS</span></span>

### <span data-ttu-id="7d3ec-134">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7d3ec-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7d3ec-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d3ec-135">OUTPUTS</span></span>

### <span data-ttu-id="7d3ec-136">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7d3ec-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7d3ec-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d3ec-137">NOTES</span></span>

## <span data-ttu-id="7d3ec-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d3ec-138">RELATED LINKS</span></span>