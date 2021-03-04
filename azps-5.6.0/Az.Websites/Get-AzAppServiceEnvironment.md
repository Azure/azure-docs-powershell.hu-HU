---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934562"
---
# <span data-ttu-id="cabf9-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="cabf9-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="cabf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabf9-102">SYNOPSIS</span></span>
<span data-ttu-id="cabf9-103">Alkalmazásszolgáltatási környezetet kap.</span><span class="sxs-lookup"><span data-stu-id="cabf9-103">Gets App Service Environment.</span></span> <span data-ttu-id="cabf9-104">Ha csak erőforráscsoport van megadva, az erőforráscsoportban visszaadja az ASE listáját.</span><span class="sxs-lookup"><span data-stu-id="cabf9-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="cabf9-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cabf9-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabf9-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cabf9-106">DESCRIPTION</span></span>
<span data-ttu-id="cabf9-107">A **Get-AzAppServiceEnvironment** parancsmag a lekérdezésnek megfelelő ASE(k)t ad vissza.</span><span class="sxs-lookup"><span data-stu-id="cabf9-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="cabf9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cabf9-108">EXAMPLES</span></span>

### <span data-ttu-id="cabf9-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="cabf9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="cabf9-110">Egy adott appszolgáltatás-környezetet ad eredményül, amely a <MyAseName> következőben van elnevezve: <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="cabf9-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="cabf9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cabf9-111">PARAMETERS</span></span>

### <span data-ttu-id="cabf9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabf9-112">-DefaultProfile</span></span>
<span data-ttu-id="cabf9-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cabf9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cabf9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cabf9-114">-Name</span></span>
<span data-ttu-id="cabf9-115">Az app szolgáltatási környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="cabf9-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabf9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabf9-116">-ResourceGroupName</span></span>
<span data-ttu-id="cabf9-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cabf9-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabf9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cabf9-118">-Confirm</span></span>
<span data-ttu-id="cabf9-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cabf9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabf9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabf9-120">-WhatIf</span></span>
<span data-ttu-id="cabf9-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cabf9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cabf9-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cabf9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabf9-123">CommonParameters</span></span>
<span data-ttu-id="cabf9-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabf9-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cabf9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabf9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cabf9-126">INPUTS</span></span>

### <span data-ttu-id="cabf9-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="cabf9-127">None</span></span>

## <span data-ttu-id="cabf9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cabf9-128">OUTPUTS</span></span>

### <span data-ttu-id="cabf9-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="cabf9-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="cabf9-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cabf9-130">NOTES</span></span>

## <span data-ttu-id="cabf9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cabf9-131">RELATED LINKS</span></span>

[<span data-ttu-id="cabf9-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="cabf9-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="cabf9-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="cabf9-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="cabf9-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="cabf9-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)