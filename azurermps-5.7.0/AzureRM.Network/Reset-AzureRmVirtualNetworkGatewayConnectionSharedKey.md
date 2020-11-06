---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504519"
---
# <span data-ttu-id="defc9-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="defc9-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="defc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="defc9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="defc9-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="defc9-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="defc9-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="defc9-104">DESCRIPTION</span></span>

## <span data-ttu-id="defc9-105">Példák</span><span class="sxs-lookup"><span data-stu-id="defc9-105">EXAMPLES</span></span>

## <span data-ttu-id="defc9-106">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="defc9-106">PARAMETERS</span></span>

### <span data-ttu-id="defc9-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defc9-107">-DefaultProfile</span></span>
<span data-ttu-id="defc9-108">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="defc9-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="defc9-109">-Force</span><span class="sxs-lookup"><span data-stu-id="defc9-109">-Force</span></span>
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

### <span data-ttu-id="defc9-110">-Karakter hossza</span><span class="sxs-lookup"><span data-stu-id="defc9-110">-KeyLength</span></span>
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

### <span data-ttu-id="defc9-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="defc9-111">-Name</span></span>
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

### <span data-ttu-id="defc9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defc9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="defc9-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="defc9-113">-Confirm</span></span>
<span data-ttu-id="defc9-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="defc9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="defc9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="defc9-115">-WhatIf</span></span>
<span data-ttu-id="defc9-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="defc9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="defc9-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="defc9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="defc9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defc9-118">CommonParameters</span></span>
<span data-ttu-id="defc9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="defc9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defc9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="defc9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defc9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="defc9-121">INPUTS</span></span>

### <span data-ttu-id="defc9-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="defc9-122">None</span></span>
<span data-ttu-id="defc9-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="defc9-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="defc9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="defc9-124">OUTPUTS</span></span>

### <span data-ttu-id="defc9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="defc9-125">System.String</span></span>

## <span data-ttu-id="defc9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="defc9-126">NOTES</span></span>

## <span data-ttu-id="defc9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="defc9-127">RELATED LINKS</span></span>

[<span data-ttu-id="defc9-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="defc9-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="defc9-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="defc9-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


