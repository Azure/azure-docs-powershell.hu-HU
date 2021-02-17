---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207015"
---
# <span data-ttu-id="37508-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="37508-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="37508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37508-102">SYNOPSIS</span></span>
<span data-ttu-id="37508-103">Társ hozzáadása Azure VirtualRouterhez</span><span class="sxs-lookup"><span data-stu-id="37508-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="37508-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37508-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37508-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37508-105">DESCRIPTION</span></span>
<span data-ttu-id="37508-106">Az **Add-AzVirtualRouterPeer** parancsmag hozzáad egy VirtualRouter-társt egy Azure VirtualRouterhez</span><span class="sxs-lookup"><span data-stu-id="37508-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="37508-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37508-107">EXAMPLES</span></span>

### <span data-ttu-id="37508-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="37508-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="37508-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37508-109">PARAMETERS</span></span>

### <span data-ttu-id="37508-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37508-110">-AsJob</span></span>
<span data-ttu-id="37508-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="37508-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37508-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37508-112">-DefaultProfile</span></span>
<span data-ttu-id="37508-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37508-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37508-114">-Force</span><span class="sxs-lookup"><span data-stu-id="37508-114">-Force</span></span>
<span data-ttu-id="37508-115">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="37508-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="37508-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="37508-116">-PeerAsn</span></span>
<span data-ttu-id="37508-117">Társközi ASN.</span><span class="sxs-lookup"><span data-stu-id="37508-117">Peer ASN.</span></span>

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

### <span data-ttu-id="37508-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="37508-118">-PeerIp</span></span>
<span data-ttu-id="37508-119">Társ ip-címe.</span><span class="sxs-lookup"><span data-stu-id="37508-119">Peer Ip.</span></span>

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

### <span data-ttu-id="37508-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="37508-120">-PeerName</span></span>
<span data-ttu-id="37508-121">A virtuális társ útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="37508-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="37508-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37508-122">-ResourceGroupName</span></span>
<span data-ttu-id="37508-123">A virtuális útválasztó/társ erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="37508-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="37508-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="37508-124">-VirtualRouterName</span></span>
<span data-ttu-id="37508-125">A virtuális útválasztó, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="37508-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="37508-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37508-126">-Confirm</span></span>
<span data-ttu-id="37508-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37508-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37508-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37508-128">-WhatIf</span></span>
<span data-ttu-id="37508-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37508-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37508-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37508-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37508-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37508-131">CommonParameters</span></span>
<span data-ttu-id="37508-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37508-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37508-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37508-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37508-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37508-134">INPUTS</span></span>

### <span data-ttu-id="37508-135">System.String</span><span class="sxs-lookup"><span data-stu-id="37508-135">System.String</span></span>

### <span data-ttu-id="37508-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="37508-136">System.UInt32</span></span>

## <span data-ttu-id="37508-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37508-137">OUTPUTS</span></span>

### <span data-ttu-id="37508-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="37508-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="37508-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37508-139">NOTES</span></span>

## <span data-ttu-id="37508-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37508-140">RELATED LINKS</span></span>
