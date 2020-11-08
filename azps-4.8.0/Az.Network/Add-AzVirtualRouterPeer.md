---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183044"
---
# <span data-ttu-id="b54a6-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="b54a6-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="b54a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b54a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b54a6-103">Egyenrangú felhasználó hozzáadása az Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b54a6-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="b54a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b54a6-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b54a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b54a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b54a6-106">Az **Add-AzVirtualRouterPeer** parancsmag egy VirtualRouter-partnert ad hozzá egy Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b54a6-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="b54a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b54a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b54a6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b54a6-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="b54a6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b54a6-109">PARAMETERS</span></span>

### <span data-ttu-id="b54a6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b54a6-110">-AsJob</span></span>
<span data-ttu-id="b54a6-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b54a6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b54a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54a6-112">-DefaultProfile</span></span>
<span data-ttu-id="b54a6-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b54a6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b54a6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b54a6-114">-Force</span></span>
<span data-ttu-id="b54a6-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b54a6-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b54a6-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b54a6-116">-PeerAsn</span></span>
<span data-ttu-id="b54a6-117">Társközi ASN.</span><span class="sxs-lookup"><span data-stu-id="b54a6-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54a6-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="b54a6-118">-PeerIp</span></span>
<span data-ttu-id="b54a6-119">Társközi IP.</span><span class="sxs-lookup"><span data-stu-id="b54a6-119">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54a6-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="b54a6-120">-PeerName</span></span>
<span data-ttu-id="b54a6-121">A virtuális útválasztó társközi neve.</span><span class="sxs-lookup"><span data-stu-id="b54a6-121">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="b54a6-123">A virtuális útválasztó/társ erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="b54a6-123">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54a6-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="b54a6-124">-VirtualRouterName</span></span>
<span data-ttu-id="b54a6-125">A virtuális útválasztó, ahol a társközi létezik.</span><span class="sxs-lookup"><span data-stu-id="b54a6-125">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54a6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b54a6-126">-Confirm</span></span>
<span data-ttu-id="b54a6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b54a6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b54a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b54a6-128">-WhatIf</span></span>
<span data-ttu-id="b54a6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b54a6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b54a6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b54a6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b54a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54a6-131">CommonParameters</span></span>
<span data-ttu-id="b54a6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b54a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54a6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b54a6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54a6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54a6-134">INPUTS</span></span>

### <span data-ttu-id="b54a6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b54a6-135">System.String</span></span>

### <span data-ttu-id="b54a6-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="b54a6-136">System.UInt32</span></span>

## <span data-ttu-id="b54a6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54a6-137">OUTPUTS</span></span>

### <span data-ttu-id="b54a6-138">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b54a6-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="b54a6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b54a6-139">NOTES</span></span>

## <span data-ttu-id="b54a6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b54a6-140">RELATED LINKS</span></span>
