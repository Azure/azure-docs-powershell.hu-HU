---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505887"
---
# <span data-ttu-id="2299b-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2299b-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="2299b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2299b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2299b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2299b-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2299b-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="2299b-104">DESCRIPTION</span></span>

## <span data-ttu-id="2299b-105">Példák</span><span class="sxs-lookup"><span data-stu-id="2299b-105">EXAMPLES</span></span>

## <span data-ttu-id="2299b-106">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2299b-106">PARAMETERS</span></span>

### <span data-ttu-id="2299b-107">-Force</span><span class="sxs-lookup"><span data-stu-id="2299b-107">-Force</span></span>
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

### <span data-ttu-id="2299b-108">-Karakter hossza</span><span class="sxs-lookup"><span data-stu-id="2299b-108">-KeyLength</span></span>
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

### <span data-ttu-id="2299b-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2299b-109">-Name</span></span>
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

### <span data-ttu-id="2299b-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2299b-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2299b-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2299b-111">-Confirm</span></span>
<span data-ttu-id="2299b-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2299b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2299b-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2299b-113">-WhatIf</span></span>
<span data-ttu-id="2299b-114">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2299b-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2299b-115">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2299b-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2299b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2299b-116">-DefaultProfile</span></span>
<span data-ttu-id="2299b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2299b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2299b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2299b-118">CommonParameters</span></span>
<span data-ttu-id="2299b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2299b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2299b-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2299b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2299b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2299b-121">INPUTS</span></span>

## <span data-ttu-id="2299b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2299b-122">OUTPUTS</span></span>

### <span data-ttu-id="2299b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2299b-123">System.String</span></span>

## <span data-ttu-id="2299b-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2299b-124">NOTES</span></span>

## <span data-ttu-id="2299b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2299b-125">RELATED LINKS</span></span>

[<span data-ttu-id="2299b-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2299b-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="2299b-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2299b-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


