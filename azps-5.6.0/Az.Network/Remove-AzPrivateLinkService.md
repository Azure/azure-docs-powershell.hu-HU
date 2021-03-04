---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: e06a29422a7abed55dbf1e8508c8715a36cf7d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941522"
---
# <span data-ttu-id="964d1-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="964d1-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="964d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964d1-102">SYNOPSIS</span></span>
<span data-ttu-id="964d1-103">Privát hivatkozásszolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="964d1-103">Removes a private link service</span></span>

## <span data-ttu-id="964d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="964d1-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="964d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="964d1-105">DESCRIPTION</span></span>
<span data-ttu-id="964d1-106">A **Remove-AzPrivateLinkService** parancsmag eltávolít egy privát hivatkozásszolgáltatást</span><span class="sxs-lookup"><span data-stu-id="964d1-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="964d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="964d1-107">EXAMPLES</span></span>

### <span data-ttu-id="964d1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="964d1-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="964d1-109">Ez a példa eltávolít egy TestPrivateLinkService nevű privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="964d1-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="964d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="964d1-110">PARAMETERS</span></span>

### <span data-ttu-id="964d1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="964d1-111">-AsJob</span></span>
<span data-ttu-id="964d1-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="964d1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="964d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964d1-113">-DefaultProfile</span></span>
<span data-ttu-id="964d1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="964d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="964d1-115">-Force</span></span>
<span data-ttu-id="964d1-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="964d1-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="964d1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="964d1-117">-Name</span></span>
<span data-ttu-id="964d1-118">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="964d1-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="964d1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="964d1-119">-PassThru</span></span>
<span data-ttu-id="964d1-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="964d1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="964d1-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="964d1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="964d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="964d1-123">A privát hivatkozásszolgáltatás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="964d1-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="964d1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="964d1-124">-Confirm</span></span>
<span data-ttu-id="964d1-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="964d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="964d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="964d1-126">-WhatIf</span></span>
<span data-ttu-id="964d1-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="964d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="964d1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="964d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="964d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964d1-129">CommonParameters</span></span>
<span data-ttu-id="964d1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964d1-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="964d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964d1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="964d1-132">INPUTS</span></span>

### <span data-ttu-id="964d1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="964d1-133">System.String</span></span>

## <span data-ttu-id="964d1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="964d1-134">OUTPUTS</span></span>

### <span data-ttu-id="964d1-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="964d1-135">System.Boolean</span></span>

## <span data-ttu-id="964d1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="964d1-136">NOTES</span></span>

## <span data-ttu-id="964d1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="964d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="964d1-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="964d1-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="964d1-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="964d1-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)