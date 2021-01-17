---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384829"
---
# <span data-ttu-id="82e81-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="82e81-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="82e81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e81-102">SYNOPSIS</span></span>
<span data-ttu-id="82e81-103">Új társközi asn-hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="82e81-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="82e81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82e81-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82e81-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82e81-105">DESCRIPTION</span></span>
<span data-ttu-id="82e81-106">Új PeerAsn-objektumot hoz létre az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="82e81-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="82e81-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82e81-107">EXAMPLES</span></span>

### <span data-ttu-id="82e81-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="82e81-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="82e81-109">Létrehoz egy új PeerAsn-t</span><span class="sxs-lookup"><span data-stu-id="82e81-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="82e81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82e81-110">PARAMETERS</span></span>

### <span data-ttu-id="82e81-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82e81-111">-AsJob</span></span>
<span data-ttu-id="82e81-112">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="82e81-112">Run in the background.</span></span>

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

### <span data-ttu-id="82e81-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="82e81-113">-ContactDetail</span></span>
<span data-ttu-id="82e81-114">A hálózati üzemeltetési központ problémáinak megoldásához használt e-mail-címek</span><span class="sxs-lookup"><span data-stu-id="82e81-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e81-115">-DefaultProfile</span></span>
<span data-ttu-id="82e81-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82e81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e81-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82e81-117">-Name</span></span>
<span data-ttu-id="82e81-118">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="82e81-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="82e81-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="82e81-119">-PeerAsn</span></span>
<span data-ttu-id="82e81-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span><span class="sxs-lookup"><span data-stu-id="82e81-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="82e81-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="82e81-121">-PeerName</span></span>
<span data-ttu-id="82e81-122">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="82e81-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="82e81-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82e81-123">-Confirm</span></span>
<span data-ttu-id="82e81-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82e81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e81-125">-WhatIf</span></span>
<span data-ttu-id="82e81-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82e81-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82e81-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82e81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e81-128">CommonParameters</span></span>
<span data-ttu-id="82e81-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e81-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82e81-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e81-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82e81-131">INPUTS</span></span>

### <span data-ttu-id="82e81-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="82e81-132">None</span></span>

## <span data-ttu-id="82e81-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82e81-133">OUTPUTS</span></span>

### <span data-ttu-id="82e81-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="82e81-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="82e81-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82e81-135">NOTES</span></span>

## <span data-ttu-id="82e81-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82e81-136">RELATED LINKS</span></span>
