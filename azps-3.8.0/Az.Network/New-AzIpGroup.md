---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011807"
---
# <span data-ttu-id="432a0-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="432a0-101">New-AzIpGroup</span></span>

## <span data-ttu-id="432a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="432a0-102">SYNOPSIS</span></span>
<span data-ttu-id="432a0-103">Azure-IpGroup hoz létre.</span><span class="sxs-lookup"><span data-stu-id="432a0-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="432a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="432a0-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="432a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="432a0-105">DESCRIPTION</span></span>
<span data-ttu-id="432a0-106">A **New-AzIpGroup** parancsmag létrehoz egy Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="432a0-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="432a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="432a0-107">EXAMPLES</span></span>

### <span data-ttu-id="432a0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="432a0-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="432a0-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="432a0-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="432a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="432a0-110">PARAMETERS</span></span>

### <span data-ttu-id="432a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="432a0-111">-AsJob</span></span>
<span data-ttu-id="432a0-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="432a0-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432a0-113">-DefaultProfile</span></span>
<span data-ttu-id="432a0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="432a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="432a0-115">-Force</span></span>
<span data-ttu-id="432a0-116">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="432a0-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-117">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="432a0-117">-IpAddress</span></span>
<span data-ttu-id="432a0-118">A IpGroup definiált IP-címek</span><span class="sxs-lookup"><span data-stu-id="432a0-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="432a0-119">-Location</span></span>
<span data-ttu-id="432a0-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="432a0-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="432a0-121">-Name</span></span>
<span data-ttu-id="432a0-122">A ipgroup neve.</span><span class="sxs-lookup"><span data-stu-id="432a0-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="432a0-124">A ipgroup erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="432a0-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="432a0-125">-Tag</span></span>
<span data-ttu-id="432a0-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="432a0-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="432a0-127">-Confirm</span></span>
<span data-ttu-id="432a0-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="432a0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432a0-129">-WhatIf</span></span>
<span data-ttu-id="432a0-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="432a0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="432a0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="432a0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432a0-132">CommonParameters</span></span>
<span data-ttu-id="432a0-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="432a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432a0-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="432a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432a0-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="432a0-135">INPUTS</span></span>

### <span data-ttu-id="432a0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="432a0-136">System.String</span></span>

### <span data-ttu-id="432a0-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="432a0-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="432a0-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="432a0-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="432a0-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="432a0-139">OUTPUTS</span></span>

### <span data-ttu-id="432a0-140">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="432a0-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="432a0-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="432a0-141">NOTES</span></span>

## <span data-ttu-id="432a0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="432a0-142">RELATED LINKS</span></span>
