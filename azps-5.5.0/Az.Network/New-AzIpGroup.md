---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154283"
---
# <span data-ttu-id="2d37f-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d37f-101">New-AzIpGroup</span></span>

## <span data-ttu-id="2d37f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d37f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d37f-103">Létrehoz egy Azure IpGroupot.</span><span class="sxs-lookup"><span data-stu-id="2d37f-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="2d37f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d37f-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d37f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d37f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d37f-106">A **New-AzIpGroup parancsmag** létrehoz egy Azure IpGroup-et</span><span class="sxs-lookup"><span data-stu-id="2d37f-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="2d37f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d37f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d37f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2d37f-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="2d37f-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="2d37f-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="2d37f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d37f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d37f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d37f-111">-AsJob</span></span>
<span data-ttu-id="2d37f-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2d37f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d37f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d37f-113">-DefaultProfile</span></span>
<span data-ttu-id="2d37f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d37f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d37f-115">-Force</span></span>
<span data-ttu-id="2d37f-116">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="2d37f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2d37f-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2d37f-117">-IpAddress</span></span>
<span data-ttu-id="2d37f-118">IpAddresses defined in the IpGroup</span><span class="sxs-lookup"><span data-stu-id="2d37f-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2d37f-119">-Location</span></span>
<span data-ttu-id="2d37f-120">A hely.</span><span class="sxs-lookup"><span data-stu-id="2d37f-120">The location.</span></span>

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

### <span data-ttu-id="2d37f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2d37f-121">-Name</span></span>
<span data-ttu-id="2d37f-122">Az IP-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d37f-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="2d37f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d37f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d37f-124">Az IP-csoport erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="2d37f-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="2d37f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d37f-125">-Tag</span></span>
<span data-ttu-id="2d37f-126">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="2d37f-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d37f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d37f-127">-Confirm</span></span>
<span data-ttu-id="2d37f-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2d37f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d37f-129">-WhatIf</span></span>
<span data-ttu-id="2d37f-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2d37f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d37f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d37f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d37f-132">CommonParameters</span></span>
<span data-ttu-id="2d37f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d37f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d37f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d37f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d37f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d37f-135">INPUTS</span></span>

### <span data-ttu-id="2d37f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2d37f-136">System.String</span></span>

### <span data-ttu-id="2d37f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d37f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="2d37f-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d37f-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d37f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d37f-139">OUTPUTS</span></span>

### <span data-ttu-id="2d37f-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d37f-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="2d37f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d37f-141">NOTES</span></span>

## <span data-ttu-id="2d37f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d37f-142">RELATED LINKS</span></span>
