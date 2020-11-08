---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012760"
---
# <span data-ttu-id="56564-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="56564-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="56564-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56564-102">SYNOPSIS</span></span>
<span data-ttu-id="56564-103">Társközi ASN eltávolítása</span><span class="sxs-lookup"><span data-stu-id="56564-103">Remove Peer Asn</span></span>

## <span data-ttu-id="56564-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56564-104">SYNTAX</span></span>

### <span data-ttu-id="56564-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="56564-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56564-106">ByName</span><span class="sxs-lookup"><span data-stu-id="56564-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56564-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="56564-107">DESCRIPTION</span></span>
<span data-ttu-id="56564-108">PeerAsn eltávolítása az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="56564-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="56564-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56564-109">EXAMPLES</span></span>

### <span data-ttu-id="56564-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56564-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="56564-111">A társközi ASN eltávolítása</span><span class="sxs-lookup"><span data-stu-id="56564-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="56564-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56564-112">PARAMETERS</span></span>

### <span data-ttu-id="56564-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56564-113">-AsJob</span></span>
<span data-ttu-id="56564-114">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="56564-114">Run in the background.</span></span>

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

### <span data-ttu-id="56564-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56564-115">-DefaultProfile</span></span>
<span data-ttu-id="56564-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56564-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56564-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56564-117">-Force</span></span>
<span data-ttu-id="56564-118">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="56564-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="56564-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56564-119">-InputObject</span></span>
<span data-ttu-id="56564-120">A PeerAsn objektum.</span><span class="sxs-lookup"><span data-stu-id="56564-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="56564-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56564-121">-Name</span></span>
<span data-ttu-id="56564-122">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="56564-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="56564-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56564-123">-PassThru</span></span>
<span data-ttu-id="56564-124">Igaz érték visszaadása befejezettként</span><span class="sxs-lookup"><span data-stu-id="56564-124">Return true if complete</span></span>

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

### <span data-ttu-id="56564-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56564-125">-Confirm</span></span>
<span data-ttu-id="56564-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56564-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56564-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56564-127">-WhatIf</span></span>
<span data-ttu-id="56564-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56564-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56564-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56564-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56564-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56564-130">CommonParameters</span></span>
<span data-ttu-id="56564-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56564-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56564-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56564-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56564-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56564-133">INPUTS</span></span>

### <span data-ttu-id="56564-134">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="56564-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="56564-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56564-135">OUTPUTS</span></span>

### <span data-ttu-id="56564-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56564-136">System.Boolean</span></span>

## <span data-ttu-id="56564-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56564-137">NOTES</span></span>

## <span data-ttu-id="56564-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56564-138">RELATED LINKS</span></span>
