---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 6b2121c581d3d7da990813884cf0097064b73f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932386"
---
# <span data-ttu-id="ab515-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ab515-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ab515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab515-102">SYNOPSIS</span></span>
<span data-ttu-id="ab515-103">Alaphelyzetbe állítja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab515-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ab515-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab515-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab515-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab515-105">DESCRIPTION</span></span>
<span data-ttu-id="ab515-106">Alaphelyzetbe állítja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab515-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ab515-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab515-107">EXAMPLES</span></span>

### <span data-ttu-id="ab515-108">1. példa:</span><span class="sxs-lookup"><span data-stu-id="ab515-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="ab515-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab515-109">PARAMETERS</span></span>

### <span data-ttu-id="ab515-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab515-110">-DefaultProfile</span></span>
<span data-ttu-id="ab515-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab515-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab515-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ab515-112">-Force</span></span>
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

### <span data-ttu-id="ab515-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="ab515-113">-KeyLength</span></span>
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

### <span data-ttu-id="ab515-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ab515-114">-Name</span></span>
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

### <span data-ttu-id="ab515-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab515-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ab515-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab515-116">-Confirm</span></span>
<span data-ttu-id="ab515-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ab515-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab515-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab515-118">-WhatIf</span></span>
<span data-ttu-id="ab515-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ab515-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab515-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab515-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab515-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab515-121">CommonParameters</span></span>
<span data-ttu-id="ab515-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab515-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab515-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab515-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab515-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab515-124">INPUTS</span></span>

### <span data-ttu-id="ab515-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ab515-125">System.String</span></span>

### <span data-ttu-id="ab515-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ab515-126">System.UInt32</span></span>

## <span data-ttu-id="ab515-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab515-127">OUTPUTS</span></span>

### <span data-ttu-id="ab515-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ab515-128">System.String</span></span>

## <span data-ttu-id="ab515-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab515-129">NOTES</span></span>

## <span data-ttu-id="ab515-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab515-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab515-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ab515-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ab515-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ab515-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
