---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186367"
---
# <span data-ttu-id="6cb81-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="6cb81-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="6cb81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cb81-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb81-103">Társközi ASN eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6cb81-103">Remove Peer Asn</span></span>

## <span data-ttu-id="6cb81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cb81-104">SYNTAX</span></span>

### <span data-ttu-id="6cb81-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cb81-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb81-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6cb81-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb81-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb81-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb81-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cb81-108">DESCRIPTION</span></span>
<span data-ttu-id="6cb81-109">PeerAsn eltávolítása az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="6cb81-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="6cb81-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6cb81-110">EXAMPLES</span></span>

### <span data-ttu-id="6cb81-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6cb81-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="6cb81-112">A társközi ASN eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6cb81-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="6cb81-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cb81-113">PARAMETERS</span></span>

### <span data-ttu-id="6cb81-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cb81-114">-AsJob</span></span>
<span data-ttu-id="6cb81-115">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="6cb81-115">Run in the background.</span></span>

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

### <span data-ttu-id="6cb81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb81-116">-DefaultProfile</span></span>
<span data-ttu-id="6cb81-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cb81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb81-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb81-118">-Force</span></span>
<span data-ttu-id="6cb81-119">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="6cb81-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="6cb81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cb81-120">-InputObject</span></span>
<span data-ttu-id="6cb81-121">A PeerAsn objektum.</span><span class="sxs-lookup"><span data-stu-id="6cb81-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb81-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cb81-122">-Name</span></span>
<span data-ttu-id="6cb81-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="6cb81-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cb81-124">-PassThru</span></span>
<span data-ttu-id="6cb81-125">Igaz érték visszaadása befejezettként</span><span class="sxs-lookup"><span data-stu-id="6cb81-125">Return true if complete</span></span>

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

### <span data-ttu-id="6cb81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cb81-126">-ResourceId</span></span>
<span data-ttu-id="6cb81-127">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="6cb81-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb81-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cb81-128">-Confirm</span></span>
<span data-ttu-id="6cb81-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cb81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb81-130">-WhatIf</span></span>
<span data-ttu-id="6cb81-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cb81-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cb81-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cb81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb81-133">CommonParameters</span></span>
<span data-ttu-id="6cb81-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cb81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb81-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6cb81-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb81-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb81-136">INPUTS</span></span>

### <span data-ttu-id="6cb81-137">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="6cb81-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="6cb81-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb81-138">System.String</span></span>

## <span data-ttu-id="6cb81-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb81-139">OUTPUTS</span></span>

### <span data-ttu-id="6cb81-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb81-140">System.Boolean</span></span>

## <span data-ttu-id="6cb81-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cb81-141">NOTES</span></span>

## <span data-ttu-id="6cb81-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb81-142">RELATED LINKS</span></span>
