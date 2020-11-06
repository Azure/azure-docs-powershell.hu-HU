---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497035"
---
# <span data-ttu-id="236e8-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="236e8-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="236e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="236e8-102">SYNOPSIS</span></span>
<span data-ttu-id="236e8-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="236e8-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="236e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="236e8-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="236e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="236e8-105">DESCRIPTION</span></span>
<span data-ttu-id="236e8-106">A **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** parancsmag a virtuális hálózati átjáró kapcsolatának megosztott kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="236e8-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="236e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="236e8-107">EXAMPLES</span></span>

## <span data-ttu-id="236e8-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="236e8-108">PARAMETERS</span></span>

### <span data-ttu-id="236e8-109">-Force</span><span class="sxs-lookup"><span data-stu-id="236e8-109">-Force</span></span>
<span data-ttu-id="236e8-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="236e8-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="236e8-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="236e8-111">-Name</span></span>
<span data-ttu-id="236e8-112">A virtuális hálózati átjáró által megosztott kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="236e8-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="236e8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236e8-113">-ResourceGroupName</span></span>
<span data-ttu-id="236e8-114">Annak az erőforráscsoport a neve, amelyhez a virtuális hálózat átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="236e8-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="236e8-115">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="236e8-115">-Value</span></span>
<span data-ttu-id="236e8-116">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="236e8-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="236e8-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="236e8-117">-Confirm</span></span>
<span data-ttu-id="236e8-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="236e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="236e8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="236e8-119">-WhatIf</span></span>
<span data-ttu-id="236e8-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="236e8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="236e8-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="236e8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="236e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236e8-122">-DefaultProfile</span></span>
<span data-ttu-id="236e8-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="236e8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="236e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236e8-124">CommonParameters</span></span>
<span data-ttu-id="236e8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="236e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236e8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236e8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="236e8-127">INPUTS</span></span>

## <span data-ttu-id="236e8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="236e8-128">OUTPUTS</span></span>

### <span data-ttu-id="236e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="236e8-129">System.String</span></span>

## <span data-ttu-id="236e8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="236e8-130">NOTES</span></span>

## <span data-ttu-id="236e8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="236e8-131">RELATED LINKS</span></span>

[<span data-ttu-id="236e8-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="236e8-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="236e8-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="236e8-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


