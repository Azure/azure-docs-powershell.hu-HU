---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2c32263d52f8e260c67395484b2a9a2e3e479ecb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929441"
---
# <span data-ttu-id="ca120-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ca120-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ca120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca120-102">SYNOPSIS</span></span>
<span data-ttu-id="ca120-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="ca120-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ca120-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca120-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca120-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca120-105">DESCRIPTION</span></span>
<span data-ttu-id="ca120-106">A **Set-AzVirtualNetworkGatewayConnectionSharedKey** parancsmag konfigurálja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ca120-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ca120-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca120-107">EXAMPLES</span></span>

### <span data-ttu-id="ca120-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ca120-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="ca120-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca120-109">PARAMETERS</span></span>

### <span data-ttu-id="ca120-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca120-110">-DefaultProfile</span></span>
<span data-ttu-id="ca120-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca120-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca120-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ca120-112">-Force</span></span>
<span data-ttu-id="ca120-113">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ca120-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca120-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ca120-114">-Name</span></span>
<span data-ttu-id="ca120-115">A virtuális hálózati átjáró megosztott kulcsának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca120-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="ca120-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca120-116">-ResourceGroupName</span></span>
<span data-ttu-id="ca120-117">Annak az erőforráscsoportnak a neve, amelyhez a virtuális hálózati átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="ca120-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="ca120-118">-Érték</span><span class="sxs-lookup"><span data-stu-id="ca120-118">-Value</span></span>
<span data-ttu-id="ca120-119">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca120-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="ca120-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca120-120">-Confirm</span></span>
<span data-ttu-id="ca120-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ca120-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca120-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca120-122">-WhatIf</span></span>
<span data-ttu-id="ca120-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ca120-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca120-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca120-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca120-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca120-125">CommonParameters</span></span>
<span data-ttu-id="ca120-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca120-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca120-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca120-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca120-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca120-128">INPUTS</span></span>

### <span data-ttu-id="ca120-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ca120-129">System.String</span></span>

## <span data-ttu-id="ca120-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca120-130">OUTPUTS</span></span>

### <span data-ttu-id="ca120-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ca120-131">System.String</span></span>

## <span data-ttu-id="ca120-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca120-132">NOTES</span></span>

## <span data-ttu-id="ca120-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca120-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca120-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ca120-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ca120-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ca120-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
