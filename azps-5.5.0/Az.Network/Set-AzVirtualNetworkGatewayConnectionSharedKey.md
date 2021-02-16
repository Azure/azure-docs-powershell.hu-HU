---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146554"
---
# <span data-ttu-id="3b573-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b573-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="3b573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b573-102">SYNOPSIS</span></span>
<span data-ttu-id="3b573-103">A virtuális hálózati átjáró kapcsolatának megosztott kulcsát konfigurálja.</span><span class="sxs-lookup"><span data-stu-id="3b573-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="3b573-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b573-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b573-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b573-105">DESCRIPTION</span></span>
<span data-ttu-id="3b573-106">A **Set-AzVirtualNetworkGatewayConnectionSharedKey** parancsmag konfigurálja a virtuális hálózati átjáró kapcsolatának megosztott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3b573-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="3b573-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b573-107">EXAMPLES</span></span>

### <span data-ttu-id="3b573-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b573-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="3b573-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b573-109">PARAMETERS</span></span>

### <span data-ttu-id="3b573-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b573-110">-DefaultProfile</span></span>
<span data-ttu-id="3b573-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b573-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b573-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3b573-112">-Force</span></span>
<span data-ttu-id="3b573-113">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3b573-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b573-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3b573-114">-Name</span></span>
<span data-ttu-id="3b573-115">A virtuális hálózati átjáró megosztott kulcsának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b573-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="3b573-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b573-116">-ResourceGroupName</span></span>
<span data-ttu-id="3b573-117">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró tartozik</span><span class="sxs-lookup"><span data-stu-id="3b573-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="3b573-118">-Érték</span><span class="sxs-lookup"><span data-stu-id="3b573-118">-Value</span></span>
<span data-ttu-id="3b573-119">A megosztott kulcs értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b573-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="3b573-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b573-120">-Confirm</span></span>
<span data-ttu-id="3b573-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3b573-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b573-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b573-122">-WhatIf</span></span>
<span data-ttu-id="3b573-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3b573-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b573-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b573-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b573-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b573-125">CommonParameters</span></span>
<span data-ttu-id="3b573-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b573-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b573-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b573-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b573-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b573-128">INPUTS</span></span>

### <span data-ttu-id="3b573-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3b573-129">System.String</span></span>

## <span data-ttu-id="3b573-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b573-130">OUTPUTS</span></span>

### <span data-ttu-id="3b573-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3b573-131">System.String</span></span>

## <span data-ttu-id="3b573-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b573-132">NOTES</span></span>

## <span data-ttu-id="3b573-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b573-133">RELATED LINKS</span></span>

[<span data-ttu-id="3b573-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b573-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="3b573-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="3b573-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
