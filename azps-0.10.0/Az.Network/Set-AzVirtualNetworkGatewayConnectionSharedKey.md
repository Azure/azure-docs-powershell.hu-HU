---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2683af757bc1b0b58ebb6865a1cfd1edeef580e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843554"
---
# <span data-ttu-id="846f8-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="846f8-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="846f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="846f8-102">SYNOPSIS</span></span>
<span data-ttu-id="846f8-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="846f8-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="846f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="846f8-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="846f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="846f8-105">DESCRIPTION</span></span>
<span data-ttu-id="846f8-106">A **set-AzVirtualNetworkGatewayConnectionSharedKey** parancsmag a virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="846f8-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="846f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="846f8-107">EXAMPLES</span></span>

### <span data-ttu-id="846f8-108">1:</span><span class="sxs-lookup"><span data-stu-id="846f8-108">1:</span></span>
```

```

## <span data-ttu-id="846f8-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="846f8-109">PARAMETERS</span></span>

### <span data-ttu-id="846f8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846f8-110">-DefaultProfile</span></span>
<span data-ttu-id="846f8-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="846f8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846f8-112">-Force</span><span class="sxs-lookup"><span data-stu-id="846f8-112">-Force</span></span>
<span data-ttu-id="846f8-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="846f8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="846f8-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="846f8-114">-Name</span></span>
<span data-ttu-id="846f8-115">A virtuális hálózati átjáró által megosztott kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="846f8-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="846f8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846f8-116">-ResourceGroupName</span></span>
<span data-ttu-id="846f8-117">Annak az erőforráscsoport a neve, amelyhez a virtuális hálózat átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="846f8-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="846f8-118">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="846f8-118">-Value</span></span>
<span data-ttu-id="846f8-119">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="846f8-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="846f8-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="846f8-120">-Confirm</span></span>
<span data-ttu-id="846f8-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="846f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846f8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846f8-122">-WhatIf</span></span>
<span data-ttu-id="846f8-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="846f8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="846f8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="846f8-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846f8-125">CommonParameters</span></span>
<span data-ttu-id="846f8-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="846f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846f8-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="846f8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846f8-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="846f8-128">INPUTS</span></span>

## <span data-ttu-id="846f8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="846f8-129">OUTPUTS</span></span>

### <span data-ttu-id="846f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="846f8-130">System.String</span></span>

## <span data-ttu-id="846f8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="846f8-131">NOTES</span></span>

## <span data-ttu-id="846f8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="846f8-132">RELATED LINKS</span></span>

[<span data-ttu-id="846f8-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="846f8-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="846f8-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="846f8-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)


