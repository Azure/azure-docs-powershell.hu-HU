---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186877"
---
# <span data-ttu-id="e2e20-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e2e20-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="e2e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2e20-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e20-103">Elérhetőségi adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="e2e20-103">Update Contact Information</span></span>

## <span data-ttu-id="e2e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2e20-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2e20-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e20-106">Lehetővé teszi, hogy az előfizetésben szereplő PeerAsn frissítse a partnerek adatait.</span><span class="sxs-lookup"><span data-stu-id="e2e20-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="e2e20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e2e20-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e20-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2e20-108">Example 1</span></span>
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

<span data-ttu-id="e2e20-109">E-mail-cím hozzáadása a társközi ASN-hoz</span><span class="sxs-lookup"><span data-stu-id="e2e20-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="e2e20-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2e20-110">PARAMETERS</span></span>

### <span data-ttu-id="e2e20-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e20-111">-AsJob</span></span>
<span data-ttu-id="e2e20-112">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e2e20-112">Run in the background.</span></span>

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

### <span data-ttu-id="e2e20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e20-113">-DefaultProfile</span></span>
<span data-ttu-id="e2e20-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2e20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e20-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e20-115">-InputObject</span></span>
<span data-ttu-id="e2e20-116">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="e2e20-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e20-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2e20-117">-Confirm</span></span>
<span data-ttu-id="e2e20-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2e20-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e20-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e20-119">-WhatIf</span></span>
<span data-ttu-id="e2e20-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2e20-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e20-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2e20-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e20-122">CommonParameters</span></span>
<span data-ttu-id="e2e20-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2e20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e20-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2e20-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e20-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2e20-125">INPUTS</span></span>

### <span data-ttu-id="e2e20-126">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e2e20-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="e2e20-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2e20-127">OUTPUTS</span></span>

### <span data-ttu-id="e2e20-128">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e2e20-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="e2e20-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2e20-129">NOTES</span></span>

## <span data-ttu-id="e2e20-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2e20-130">RELATED LINKS</span></span>
