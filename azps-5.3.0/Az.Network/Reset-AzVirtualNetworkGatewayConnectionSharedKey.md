---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481164"
---
# <span data-ttu-id="71a27-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="71a27-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="71a27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71a27-102">SYNOPSIS</span></span>
<span data-ttu-id="71a27-103">Alaphelyzetbe állítja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="71a27-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="71a27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71a27-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71a27-105">DESCRIPTION</span></span>
<span data-ttu-id="71a27-106">Alaphelyzetbe állítja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="71a27-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="71a27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71a27-107">EXAMPLES</span></span>

### <span data-ttu-id="71a27-108">1. példa:</span><span class="sxs-lookup"><span data-stu-id="71a27-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="71a27-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71a27-109">PARAMETERS</span></span>

### <span data-ttu-id="71a27-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a27-110">-DefaultProfile</span></span>
<span data-ttu-id="71a27-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71a27-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71a27-112">-Force</span><span class="sxs-lookup"><span data-stu-id="71a27-112">-Force</span></span>
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

### <span data-ttu-id="71a27-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="71a27-113">-KeyLength</span></span>
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

### <span data-ttu-id="71a27-114">-Name</span><span class="sxs-lookup"><span data-stu-id="71a27-114">-Name</span></span>
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

### <span data-ttu-id="71a27-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a27-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="71a27-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a27-116">-Confirm</span></span>
<span data-ttu-id="71a27-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71a27-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a27-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a27-118">-WhatIf</span></span>
<span data-ttu-id="71a27-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71a27-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a27-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71a27-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a27-121">CommonParameters</span></span>
<span data-ttu-id="71a27-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a27-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a27-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a27-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71a27-124">INPUTS</span></span>

### <span data-ttu-id="71a27-125">System.String</span><span class="sxs-lookup"><span data-stu-id="71a27-125">System.String</span></span>

### <span data-ttu-id="71a27-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="71a27-126">System.UInt32</span></span>

## <span data-ttu-id="71a27-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71a27-127">OUTPUTS</span></span>

### <span data-ttu-id="71a27-128">System.String</span><span class="sxs-lookup"><span data-stu-id="71a27-128">System.String</span></span>

## <span data-ttu-id="71a27-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71a27-129">NOTES</span></span>

## <span data-ttu-id="71a27-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71a27-130">RELATED LINKS</span></span>

[<span data-ttu-id="71a27-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="71a27-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="71a27-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="71a27-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
