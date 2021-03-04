---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939057"
---
# <span data-ttu-id="0075f-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="0075f-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="0075f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0075f-102">SYNOPSIS</span></span>
<span data-ttu-id="0075f-103">ExpressRoute-kapcsolati kapcsolatengedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0075f-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0075f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0075f-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0075f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0075f-105">DESCRIPTION</span></span>
<span data-ttu-id="0075f-106">ExpressRoute-kapcsolati kapcsolatengedély létrehozása vagy frissítése privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0075f-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0075f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0075f-107">EXAMPLES</span></span>

### <span data-ttu-id="0075f-108">1. példa: Automatikus javítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0075f-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="0075f-109">Ez a parancsmag hitelesítést hoz létre `azps-test-auth` a privát felhőben `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="0075f-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="0075f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0075f-110">PARAMETERS</span></span>

### <span data-ttu-id="0075f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0075f-111">-AsJob</span></span>
<span data-ttu-id="0075f-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="0075f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0075f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0075f-113">-DefaultProfile</span></span>
<span data-ttu-id="0075f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0075f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0075f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0075f-115">-Name</span></span>
<span data-ttu-id="0075f-116">Az ExpressRoute-kapcsolat kapcsolati engedélyének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="0075f-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="0075f-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0075f-117">-NoWait</span></span>
<span data-ttu-id="0075f-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="0075f-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0075f-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0075f-119">-PrivateCloudName</span></span>
<span data-ttu-id="0075f-120">A privát felhő neve.</span><span class="sxs-lookup"><span data-stu-id="0075f-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="0075f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0075f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0075f-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0075f-122">The name of the resource group.</span></span>
<span data-ttu-id="0075f-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="0075f-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0075f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0075f-124">-SubscriptionId</span></span>
<span data-ttu-id="0075f-125">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0075f-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0075f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0075f-126">-Confirm</span></span>
<span data-ttu-id="0075f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0075f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0075f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0075f-128">-WhatIf</span></span>
<span data-ttu-id="0075f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0075f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0075f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0075f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0075f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0075f-131">CommonParameters</span></span>
<span data-ttu-id="0075f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0075f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0075f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0075f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0075f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0075f-134">INPUTS</span></span>

## <span data-ttu-id="0075f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0075f-135">OUTPUTS</span></span>

### <span data-ttu-id="0075f-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="0075f-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="0075f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0075f-137">NOTES</span></span>

<span data-ttu-id="0075f-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0075f-138">ALIASES</span></span>

## <span data-ttu-id="0075f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0075f-139">RELATED LINKS</span></span>

