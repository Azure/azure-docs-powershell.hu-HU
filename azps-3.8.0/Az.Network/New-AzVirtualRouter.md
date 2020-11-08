---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013222"
---
# <span data-ttu-id="232c1-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="232c1-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="232c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="232c1-102">SYNOPSIS</span></span>
<span data-ttu-id="232c1-103">Azure-VirtualRouter hoz létre.</span><span class="sxs-lookup"><span data-stu-id="232c1-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="232c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="232c1-104">SYNTAX</span></span>

### <span data-ttu-id="232c1-105">HostedGatewayParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="232c1-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232c1-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="232c1-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="232c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="232c1-107">DESCRIPTION</span></span>
<span data-ttu-id="232c1-108">A **New-AzVirtualRouter** parancsmag létrehoz egy Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="232c1-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="232c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="232c1-109">EXAMPLES</span></span>

### <span data-ttu-id="232c1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="232c1-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="232c1-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="232c1-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="232c1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="232c1-112">PARAMETERS</span></span>

### <span data-ttu-id="232c1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="232c1-113">-AsJob</span></span>
<span data-ttu-id="232c1-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="232c1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="232c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232c1-115">-DefaultProfile</span></span>
<span data-ttu-id="232c1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="232c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="232c1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="232c1-117">-Force</span></span>
<span data-ttu-id="232c1-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="232c1-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="232c1-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="232c1-119">-HostedGateway</span></span>
<span data-ttu-id="232c1-120">Az az átjáró, ahol a virtuális útválasztót üzemeltetni kell.</span><span class="sxs-lookup"><span data-stu-id="232c1-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232c1-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="232c1-121">-HostedGatewayId</span></span>
<span data-ttu-id="232c1-122">Annak az átjárónak az azonosítója, amelyen a virtuális útválasztót üzemeltetni kell.</span><span class="sxs-lookup"><span data-stu-id="232c1-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232c1-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="232c1-123">-Location</span></span>
<span data-ttu-id="232c1-124">A hely.</span><span class="sxs-lookup"><span data-stu-id="232c1-124">The location.</span></span>

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

### <span data-ttu-id="232c1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="232c1-125">-Name</span></span>
<span data-ttu-id="232c1-126">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="232c1-126">The name of the virtual router.</span></span>

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

### <span data-ttu-id="232c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="232c1-128">A virtuális útválasztó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="232c1-128">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="232c1-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="232c1-129">-Tag</span></span>
<span data-ttu-id="232c1-130">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="232c1-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="232c1-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="232c1-131">-Confirm</span></span>
<span data-ttu-id="232c1-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="232c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232c1-133">-WhatIf</span></span>
<span data-ttu-id="232c1-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="232c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232c1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="232c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232c1-136">CommonParameters</span></span>
<span data-ttu-id="232c1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="232c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="232c1-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232c1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232c1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="232c1-139">INPUTS</span></span>

### <span data-ttu-id="232c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="232c1-140">System.String</span></span>

### <span data-ttu-id="232c1-141">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="232c1-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="232c1-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="232c1-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="232c1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="232c1-143">OUTPUTS</span></span>

### <span data-ttu-id="232c1-144">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="232c1-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="232c1-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="232c1-145">NOTES</span></span>

## <span data-ttu-id="232c1-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="232c1-146">RELATED LINKS</span></span>
