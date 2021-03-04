---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: fd4058cd09ad0d0ca27f8324368cd6d0277cec7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937578"
---
# <span data-ttu-id="050e3-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="050e3-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="050e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050e3-102">SYNOPSIS</span></span>
<span data-ttu-id="050e3-103">Névjegyinformációk frissítése</span><span class="sxs-lookup"><span data-stu-id="050e3-103">Update Contact Information</span></span>

## <span data-ttu-id="050e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="050e3-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="050e3-105">DESCRIPTION</span></span>
<span data-ttu-id="050e3-106">Lehetővé teszi, hogy frissítse egy PeerAsn-partner adatait az előfizetésen.</span><span class="sxs-lookup"><span data-stu-id="050e3-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="050e3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="050e3-107">EXAMPLES</span></span>

### <span data-ttu-id="050e3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="050e3-108">Example 1</span></span>
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

<span data-ttu-id="050e3-109">E-mail-cím hozzáadása a Társ asn programhoz</span><span class="sxs-lookup"><span data-stu-id="050e3-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="050e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="050e3-110">PARAMETERS</span></span>

### <span data-ttu-id="050e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="050e3-111">-AsJob</span></span>
<span data-ttu-id="050e3-112">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="050e3-112">Run in the background.</span></span>

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

### <span data-ttu-id="050e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050e3-113">-DefaultProfile</span></span>
<span data-ttu-id="050e3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="050e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050e3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="050e3-115">-InputObject</span></span>
<span data-ttu-id="050e3-116">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="050e3-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="050e3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="050e3-117">-Confirm</span></span>
<span data-ttu-id="050e3-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="050e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050e3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050e3-119">-WhatIf</span></span>
<span data-ttu-id="050e3-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="050e3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="050e3-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="050e3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050e3-122">CommonParameters</span></span>
<span data-ttu-id="050e3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050e3-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="050e3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050e3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="050e3-125">INPUTS</span></span>

### <span data-ttu-id="050e3-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="050e3-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="050e3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="050e3-127">OUTPUTS</span></span>

### <span data-ttu-id="050e3-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="050e3-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="050e3-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="050e3-129">NOTES</span></span>

## <span data-ttu-id="050e3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="050e3-130">RELATED LINKS</span></span>
