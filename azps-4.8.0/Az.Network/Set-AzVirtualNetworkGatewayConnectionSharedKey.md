---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184053"
---
# <span data-ttu-id="48afd-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="48afd-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="48afd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48afd-102">SYNOPSIS</span></span>
<span data-ttu-id="48afd-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="48afd-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="48afd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48afd-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48afd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48afd-105">DESCRIPTION</span></span>
<span data-ttu-id="48afd-106">A **set-AzVirtualNetworkGatewayConnectionSharedKey** parancsmag a virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="48afd-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="48afd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48afd-107">EXAMPLES</span></span>

### <span data-ttu-id="48afd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48afd-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="48afd-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48afd-109">PARAMETERS</span></span>

### <span data-ttu-id="48afd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48afd-110">-DefaultProfile</span></span>
<span data-ttu-id="48afd-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48afd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48afd-112">-Force</span><span class="sxs-lookup"><span data-stu-id="48afd-112">-Force</span></span>
<span data-ttu-id="48afd-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="48afd-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48afd-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48afd-114">-Name</span></span>
<span data-ttu-id="48afd-115">A virtuális hálózati átjáró által megosztott kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48afd-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="48afd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48afd-116">-ResourceGroupName</span></span>
<span data-ttu-id="48afd-117">Annak az erőforráscsoport a neve, amelyhez a virtuális hálózat átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="48afd-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="48afd-118">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="48afd-118">-Value</span></span>
<span data-ttu-id="48afd-119">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48afd-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="48afd-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48afd-120">-Confirm</span></span>
<span data-ttu-id="48afd-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48afd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48afd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48afd-122">-WhatIf</span></span>
<span data-ttu-id="48afd-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48afd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48afd-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48afd-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48afd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48afd-125">CommonParameters</span></span>
<span data-ttu-id="48afd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48afd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48afd-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48afd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48afd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48afd-128">INPUTS</span></span>

### <span data-ttu-id="48afd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="48afd-129">System.String</span></span>

## <span data-ttu-id="48afd-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48afd-130">OUTPUTS</span></span>

### <span data-ttu-id="48afd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48afd-131">System.String</span></span>

## <span data-ttu-id="48afd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48afd-132">NOTES</span></span>

## <span data-ttu-id="48afd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48afd-133">RELATED LINKS</span></span>

[<span data-ttu-id="48afd-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="48afd-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="48afd-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="48afd-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
