---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850602"
---
# <span data-ttu-id="c8756-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c8756-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c8756-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8756-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8756-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8756-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8756-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8756-104">DESCRIPTION</span></span>

## <span data-ttu-id="c8756-105">Példák</span><span class="sxs-lookup"><span data-stu-id="c8756-105">EXAMPLES</span></span>

### <span data-ttu-id="c8756-106">1:</span><span class="sxs-lookup"><span data-stu-id="c8756-106">1:</span></span>
```

```

## <span data-ttu-id="c8756-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8756-107">PARAMETERS</span></span>

### <span data-ttu-id="c8756-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8756-108">-DefaultProfile</span></span>
<span data-ttu-id="c8756-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8756-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8756-110">-Force</span><span class="sxs-lookup"><span data-stu-id="c8756-110">-Force</span></span>
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

### <span data-ttu-id="c8756-111">-Karakter hossza</span><span class="sxs-lookup"><span data-stu-id="c8756-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8756-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8756-112">-Name</span></span>
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

### <span data-ttu-id="c8756-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8756-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c8756-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8756-114">-Confirm</span></span>
<span data-ttu-id="c8756-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8756-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8756-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8756-116">-WhatIf</span></span>
<span data-ttu-id="c8756-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8756-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8756-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8756-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8756-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8756-119">CommonParameters</span></span>
<span data-ttu-id="c8756-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8756-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8756-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8756-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8756-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8756-122">INPUTS</span></span>

## <span data-ttu-id="c8756-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8756-123">OUTPUTS</span></span>

### <span data-ttu-id="c8756-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c8756-124">System.String</span></span>

## <span data-ttu-id="c8756-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8756-125">NOTES</span></span>

## <span data-ttu-id="c8756-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8756-126">RELATED LINKS</span></span>

[<span data-ttu-id="c8756-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c8756-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c8756-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c8756-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


