---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206694"
---
# <span data-ttu-id="e3d75-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e3d75-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e3d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d75-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d75-103">Háttércímkészlet-konfigurációt hoz létre a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="e3d75-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e3d75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3d75-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d75-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3d75-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d75-106">A **New-AzLoadBalancerBackendAddressPoolConfig** parancsmag létrehoz egy háttércímkészlet-konfigurációt egy Azure terheléselegyenítő számára.</span><span class="sxs-lookup"><span data-stu-id="e3d75-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e3d75-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3d75-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d75-108">1. példa: Háttércímkészlet-konfiguráció létrehozása terheléselosztáshoz</span><span class="sxs-lookup"><span data-stu-id="e3d75-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e3d75-109">Ez a parancs létrehoz egy BackendAddressPool02 nevű háttércímkészlet-konfigurációt a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="e3d75-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e3d75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d75-110">PARAMETERS</span></span>

### <span data-ttu-id="e3d75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d75-111">-DefaultProfile</span></span>
<span data-ttu-id="e3d75-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3d75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d75-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d75-113">-Name</span></span>
<span data-ttu-id="e3d75-114">A létrehozni szükséges címkészlet-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3d75-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d75-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3d75-115">-Confirm</span></span>
<span data-ttu-id="e3d75-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3d75-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d75-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d75-117">-WhatIf</span></span>
<span data-ttu-id="e3d75-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3d75-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3d75-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3d75-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d75-120">CommonParameters</span></span>
<span data-ttu-id="e3d75-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d75-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d75-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d75-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3d75-123">INPUTS</span></span>

### <span data-ttu-id="e3d75-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3d75-124">None</span></span>

## <span data-ttu-id="e3d75-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3d75-125">OUTPUTS</span></span>

### <span data-ttu-id="e3d75-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e3d75-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e3d75-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3d75-127">NOTES</span></span>

## <span data-ttu-id="e3d75-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3d75-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3d75-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e3d75-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e3d75-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e3d75-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e3d75-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e3d75-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


