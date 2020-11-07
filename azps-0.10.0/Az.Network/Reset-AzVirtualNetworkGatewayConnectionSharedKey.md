---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843733"
---
# <span data-ttu-id="370bb-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="370bb-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="370bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="370bb-102">SYNOPSIS</span></span>

## <span data-ttu-id="370bb-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="370bb-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="370bb-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="370bb-104">DESCRIPTION</span></span>

## <span data-ttu-id="370bb-105">Példák</span><span class="sxs-lookup"><span data-stu-id="370bb-105">EXAMPLES</span></span>

### <span data-ttu-id="370bb-106">1:</span><span class="sxs-lookup"><span data-stu-id="370bb-106">1:</span></span>
```

```

## <span data-ttu-id="370bb-107">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="370bb-107">PARAMETERS</span></span>

### <span data-ttu-id="370bb-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370bb-108">-DefaultProfile</span></span>
<span data-ttu-id="370bb-109">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="370bb-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="370bb-110">-Force</span><span class="sxs-lookup"><span data-stu-id="370bb-110">-Force</span></span>
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

### <span data-ttu-id="370bb-111">-Karakter hossza</span><span class="sxs-lookup"><span data-stu-id="370bb-111">-KeyLength</span></span>
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

### <span data-ttu-id="370bb-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="370bb-112">-Name</span></span>
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

### <span data-ttu-id="370bb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370bb-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="370bb-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="370bb-114">-Confirm</span></span>
<span data-ttu-id="370bb-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="370bb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370bb-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370bb-116">-WhatIf</span></span>
<span data-ttu-id="370bb-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="370bb-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370bb-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="370bb-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370bb-119">CommonParameters</span></span>
<span data-ttu-id="370bb-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="370bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370bb-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370bb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370bb-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="370bb-122">INPUTS</span></span>

## <span data-ttu-id="370bb-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="370bb-123">OUTPUTS</span></span>

### <span data-ttu-id="370bb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="370bb-124">System.String</span></span>

## <span data-ttu-id="370bb-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="370bb-125">NOTES</span></span>

## <span data-ttu-id="370bb-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="370bb-126">RELATED LINKS</span></span>

[<span data-ttu-id="370bb-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="370bb-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="370bb-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="370bb-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


