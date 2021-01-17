---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481201"
---
# <span data-ttu-id="fee53-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fee53-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="fee53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee53-102">SYNOPSIS</span></span>
<span data-ttu-id="fee53-103">Privát hivatkozásszolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fee53-103">Removes a private link service</span></span>

## <span data-ttu-id="fee53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fee53-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee53-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fee53-105">DESCRIPTION</span></span>
<span data-ttu-id="fee53-106">A **Remove-AzPrivateLinkService** parancsmag eltávolít egy privát hivatkozásszolgáltatást</span><span class="sxs-lookup"><span data-stu-id="fee53-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="fee53-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fee53-107">EXAMPLES</span></span>

### <span data-ttu-id="fee53-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fee53-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="fee53-109">Ez a példa eltávolít egy TestPrivateLinkService nevű privát hivatkozásszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="fee53-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="fee53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee53-110">PARAMETERS</span></span>

### <span data-ttu-id="fee53-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fee53-111">-AsJob</span></span>
<span data-ttu-id="fee53-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fee53-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fee53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee53-113">-DefaultProfile</span></span>
<span data-ttu-id="fee53-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fee53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee53-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fee53-115">-Force</span></span>
<span data-ttu-id="fee53-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="fee53-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fee53-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fee53-117">-Name</span></span>
<span data-ttu-id="fee53-118">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="fee53-118">The name of the service.</span></span>

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

### <span data-ttu-id="fee53-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fee53-119">-PassThru</span></span>
<span data-ttu-id="fee53-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="fee53-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fee53-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fee53-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fee53-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee53-122">-ResourceGroupName</span></span>
<span data-ttu-id="fee53-123">A privát hivatkozásszolgáltatás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="fee53-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="fee53-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee53-124">-Confirm</span></span>
<span data-ttu-id="fee53-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fee53-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee53-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee53-126">-WhatIf</span></span>
<span data-ttu-id="fee53-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fee53-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee53-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fee53-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee53-129">CommonParameters</span></span>
<span data-ttu-id="fee53-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee53-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee53-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee53-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee53-132">INPUTS</span></span>

### <span data-ttu-id="fee53-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fee53-133">System.String</span></span>

## <span data-ttu-id="fee53-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fee53-134">OUTPUTS</span></span>

### <span data-ttu-id="fee53-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fee53-135">System.Boolean</span></span>

## <span data-ttu-id="fee53-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fee53-136">NOTES</span></span>

## <span data-ttu-id="fee53-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fee53-137">RELATED LINKS</span></span>

[<span data-ttu-id="fee53-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fee53-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="fee53-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fee53-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)