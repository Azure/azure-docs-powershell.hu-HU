---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380825"
---
# <span data-ttu-id="f9568-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="f9568-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="f9568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9568-102">SYNOPSIS</span></span>
<span data-ttu-id="f9568-103">ExpressRoute-kapcsolati kapcsolatengedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="f9568-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f9568-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9568-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f9568-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9568-105">DESCRIPTION</span></span>
<span data-ttu-id="f9568-106">ExpressRoute-kapcsolati kapcsolatengedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="f9568-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="f9568-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9568-107">EXAMPLES</span></span>

### <span data-ttu-id="f9568-108">1. példa: Automatikus javítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f9568-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="f9568-109">Ez a parancsmag hitelesítést hoz létre `azps-test-auth` a privát felhőben `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="f9568-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="f9568-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9568-110">PARAMETERS</span></span>

### <span data-ttu-id="f9568-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9568-111">-AsJob</span></span>
<span data-ttu-id="f9568-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f9568-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f9568-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9568-113">-DefaultProfile</span></span>
<span data-ttu-id="f9568-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9568-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9568-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f9568-115">-Name</span></span>
<span data-ttu-id="f9568-116">Az ExpressRoute-kapcsolat kapcsolati engedélyének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="f9568-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9568-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f9568-117">-NoWait</span></span>
<span data-ttu-id="f9568-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f9568-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f9568-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f9568-119">-PrivateCloudName</span></span>
<span data-ttu-id="f9568-120">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="f9568-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="f9568-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9568-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9568-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9568-122">The name of the resource group.</span></span>
<span data-ttu-id="f9568-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="f9568-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f9568-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9568-124">-SubscriptionId</span></span>
<span data-ttu-id="f9568-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9568-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9568-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9568-126">-Confirm</span></span>
<span data-ttu-id="f9568-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9568-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9568-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9568-128">-WhatIf</span></span>
<span data-ttu-id="f9568-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9568-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9568-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9568-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9568-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9568-131">CommonParameters</span></span>
<span data-ttu-id="f9568-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9568-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9568-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9568-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9568-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9568-134">INPUTS</span></span>

## <span data-ttu-id="f9568-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9568-135">OUTPUTS</span></span>

### <span data-ttu-id="f9568-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="f9568-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="f9568-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9568-137">NOTES</span></span>

<span data-ttu-id="f9568-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f9568-138">ALIASES</span></span>

## <span data-ttu-id="f9568-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9568-139">RELATED LINKS</span></span>

