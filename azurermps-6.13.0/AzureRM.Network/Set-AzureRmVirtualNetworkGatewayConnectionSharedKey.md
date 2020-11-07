---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: f3268d78ac0630e18307646086689cb8d435c290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672913"
---
# <span data-ttu-id="5fb4e-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5fb4e-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="5fb4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb4e-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fb4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fb4e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb4e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fb4e-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb4e-106">A **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** parancsmag a virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="5fb4e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fb4e-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb4e-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="5fb4e-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="5fb4e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fb4e-109">PARAMETERS</span></span>

### <span data-ttu-id="5fb4e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb4e-110">-DefaultProfile</span></span>
<span data-ttu-id="5fb4e-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb4e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="5fb4e-112">-Force</span></span>
<span data-ttu-id="5fb4e-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5fb4e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fb4e-114">-Name</span></span>
<span data-ttu-id="5fb4e-115">A virtuális hálózati átjáró által megosztott kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="5fb4e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb4e-116">-ResourceGroupName</span></span>
<span data-ttu-id="5fb4e-117">Annak az erőforráscsoport a neve, amelyhez a virtuális hálózat átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="5fb4e-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="5fb4e-118">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="5fb4e-118">-Value</span></span>
<span data-ttu-id="5fb4e-119">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="5fb4e-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fb4e-120">-Confirm</span></span>
<span data-ttu-id="5fb4e-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb4e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb4e-122">-WhatIf</span></span>
<span data-ttu-id="5fb4e-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb4e-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fb4e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb4e-125">CommonParameters</span></span>
<span data-ttu-id="5fb4e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fb4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb4e-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb4e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb4e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb4e-128">INPUTS</span></span>

### <span data-ttu-id="5fb4e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb4e-129">System.String</span></span>

## <span data-ttu-id="5fb4e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb4e-130">OUTPUTS</span></span>

### <span data-ttu-id="5fb4e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb4e-131">System.String</span></span>

## <span data-ttu-id="5fb4e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fb4e-132">NOTES</span></span>

## <span data-ttu-id="5fb4e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fb4e-133">RELATED LINKS</span></span>

[<span data-ttu-id="5fb4e-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5fb4e-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="5fb4e-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="5fb4e-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


