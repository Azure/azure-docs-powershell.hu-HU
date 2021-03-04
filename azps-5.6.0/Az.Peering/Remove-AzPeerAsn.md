---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937633"
---
# <span data-ttu-id="631f2-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="631f2-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="631f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631f2-102">SYNOPSIS</span></span>
<span data-ttu-id="631f2-103">Társ asn eltávolítása</span><span class="sxs-lookup"><span data-stu-id="631f2-103">Remove Peer Asn</span></span>

## <span data-ttu-id="631f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="631f2-104">SYNTAX</span></span>

### <span data-ttu-id="631f2-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="631f2-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631f2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="631f2-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631f2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="631f2-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631f2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="631f2-108">DESCRIPTION</span></span>
<span data-ttu-id="631f2-109">Távolítson el egy PeerAsn-t az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="631f2-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="631f2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="631f2-110">EXAMPLES</span></span>

### <span data-ttu-id="631f2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="631f2-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="631f2-112">A Társ asn eltávolítása</span><span class="sxs-lookup"><span data-stu-id="631f2-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="631f2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631f2-113">PARAMETERS</span></span>

### <span data-ttu-id="631f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="631f2-114">-AsJob</span></span>
<span data-ttu-id="631f2-115">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="631f2-115">Run in the background.</span></span>

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

### <span data-ttu-id="631f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631f2-116">-DefaultProfile</span></span>
<span data-ttu-id="631f2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="631f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631f2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="631f2-118">-Force</span></span>
<span data-ttu-id="631f2-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="631f2-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="631f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="631f2-120">-InputObject</span></span>
<span data-ttu-id="631f2-121">A PeerAsn objektum.</span><span class="sxs-lookup"><span data-stu-id="631f2-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="631f2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="631f2-122">-Name</span></span>
<span data-ttu-id="631f2-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="631f2-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="631f2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="631f2-124">-PassThru</span></span>
<span data-ttu-id="631f2-125">Return true if complete</span><span class="sxs-lookup"><span data-stu-id="631f2-125">Return true if complete</span></span>

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

### <span data-ttu-id="631f2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="631f2-126">-ResourceId</span></span>
<span data-ttu-id="631f2-127">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="631f2-127">The resource id string name.</span></span>

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

### <span data-ttu-id="631f2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="631f2-128">-Confirm</span></span>
<span data-ttu-id="631f2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="631f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631f2-130">-WhatIf</span></span>
<span data-ttu-id="631f2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="631f2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="631f2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="631f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631f2-133">CommonParameters</span></span>
<span data-ttu-id="631f2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631f2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631f2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="631f2-136">INPUTS</span></span>

### <span data-ttu-id="631f2-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="631f2-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="631f2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="631f2-138">System.String</span></span>

## <span data-ttu-id="631f2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="631f2-139">OUTPUTS</span></span>

### <span data-ttu-id="631f2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="631f2-140">System.Boolean</span></span>

## <span data-ttu-id="631f2-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="631f2-141">NOTES</span></span>

## <span data-ttu-id="631f2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="631f2-142">RELATED LINKS</span></span>
