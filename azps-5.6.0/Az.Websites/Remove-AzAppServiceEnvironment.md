---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927657"
---
# <span data-ttu-id="2dda4-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="2dda4-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="2dda4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dda4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dda4-103">Távolítsa el az app szolgáltatási környezetét.</span><span class="sxs-lookup"><span data-stu-id="2dda4-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="2dda4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2dda4-104">SYNTAX</span></span>

### <span data-ttu-id="2dda4-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dda4-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dda4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dda4-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dda4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2dda4-107">DESCRIPTION</span></span>
<span data-ttu-id="2dda4-108">A **Remove-AzAppServiceEnvironment** parancsmag eltávolítja az appszolgáltatási környezetet.</span><span class="sxs-lookup"><span data-stu-id="2dda4-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="2dda4-109">Az ASE törlése előtt minden appszolgáltatást törölni kell.</span><span class="sxs-lookup"><span data-stu-id="2dda4-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="2dda4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2dda4-110">EXAMPLES</span></span>

### <span data-ttu-id="2dda4-111">1. példa: App szolgáltatási környezet törlése</span><span class="sxs-lookup"><span data-stu-id="2dda4-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="2dda4-112">App szolgáltatási környezet törlése</span><span class="sxs-lookup"><span data-stu-id="2dda4-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="2dda4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dda4-113">PARAMETERS</span></span>

### <span data-ttu-id="2dda4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dda4-114">-AsJob</span></span>
<span data-ttu-id="2dda4-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="2dda4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2dda4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dda4-116">-DefaultProfile</span></span>
<span data-ttu-id="2dda4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2dda4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dda4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2dda4-118">-Force</span></span>
<span data-ttu-id="2dda4-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2dda4-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2dda4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dda4-120">-InputObject</span></span>
<span data-ttu-id="2dda4-121">Az app szolgáltatási környezetének objektuma</span><span class="sxs-lookup"><span data-stu-id="2dda4-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2dda4-122">-Name</span></span>
<span data-ttu-id="2dda4-123">Az app szolgáltatási környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="2dda4-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dda4-124">-PassThru</span></span>
<span data-ttu-id="2dda4-125">Visszaküldés állapota.</span><span class="sxs-lookup"><span data-stu-id="2dda4-125">Return status.</span></span>

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

### <span data-ttu-id="2dda4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dda4-126">-ResourceGroupName</span></span>
<span data-ttu-id="2dda4-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dda4-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dda4-128">-Confirm</span></span>
<span data-ttu-id="2dda4-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2dda4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dda4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dda4-130">-WhatIf</span></span>
<span data-ttu-id="2dda4-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2dda4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dda4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2dda4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dda4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dda4-133">CommonParameters</span></span>
<span data-ttu-id="2dda4-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dda4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dda4-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dda4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dda4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dda4-136">INPUTS</span></span>

### <span data-ttu-id="2dda4-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="2dda4-137">None</span></span>

## <span data-ttu-id="2dda4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dda4-138">OUTPUTS</span></span>

### <span data-ttu-id="2dda4-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="2dda4-139">System.Object</span></span>
## <span data-ttu-id="2dda4-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2dda4-140">NOTES</span></span>

## <span data-ttu-id="2dda4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dda4-141">RELATED LINKS</span></span>

[<span data-ttu-id="2dda4-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="2dda4-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="2dda4-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="2dda4-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="2dda4-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="2dda4-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)