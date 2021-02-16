---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209231"
---
# <span data-ttu-id="7c314-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7c314-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="7c314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c314-102">SYNOPSIS</span></span>
<span data-ttu-id="7c314-103">Kusto-fürt egyszerű hozzárendelése.</span><span class="sxs-lookup"><span data-stu-id="7c314-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7c314-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c314-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c314-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c314-105">DESCRIPTION</span></span>
<span data-ttu-id="7c314-106">Kusto-fürt egyszerű hozzárendelése.</span><span class="sxs-lookup"><span data-stu-id="7c314-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7c314-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c314-107">EXAMPLES</span></span>

### <span data-ttu-id="7c314-108">1. példa: Kusto-fürt egyszerű hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="7c314-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="7c314-109">A fenti parancs egy Kusto-fürt egyszerű hozzárendelését hozza létre</span><span class="sxs-lookup"><span data-stu-id="7c314-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="7c314-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c314-110">PARAMETERS</span></span>

### <span data-ttu-id="7c314-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c314-111">-AsJob</span></span>
<span data-ttu-id="7c314-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7c314-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7c314-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7c314-113">-ClusterName</span></span>
<span data-ttu-id="7c314-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7c314-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7c314-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c314-115">-DefaultProfile</span></span>
<span data-ttu-id="7c314-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c314-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c314-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c314-117">-NoWait</span></span>
<span data-ttu-id="7c314-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7c314-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c314-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7c314-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="7c314-120">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="7c314-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="7c314-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="7c314-121">-PrincipalId</span></span>
<span data-ttu-id="7c314-122">A fürtnévhez rendelt egyszerű azonosító.</span><span class="sxs-lookup"><span data-stu-id="7c314-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="7c314-123">Ez lehet egy felhasználói e-mail-cím, alkalmazásazonosító vagy biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c314-123">It can be a user email, application ID, or security group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c314-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="7c314-124">-PrincipalType</span></span>
<span data-ttu-id="7c314-125">Egyszerű típus.</span><span class="sxs-lookup"><span data-stu-id="7c314-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c314-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c314-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c314-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c314-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7c314-128">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="7c314-128">-Role</span></span>
<span data-ttu-id="7c314-129">Fürtvezető szerepkör.</span><span class="sxs-lookup"><span data-stu-id="7c314-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c314-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c314-130">-SubscriptionId</span></span>
<span data-ttu-id="7c314-131">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7c314-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c314-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7c314-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7c314-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7c314-133">-TenantId</span></span>
<span data-ttu-id="7c314-134">A tőkenév bérlőazonosítója</span><span class="sxs-lookup"><span data-stu-id="7c314-134">The tenant id of the principal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c314-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c314-135">-Confirm</span></span>
<span data-ttu-id="7c314-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c314-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c314-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c314-137">-WhatIf</span></span>
<span data-ttu-id="7c314-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c314-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c314-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c314-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c314-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c314-140">CommonParameters</span></span>
<span data-ttu-id="7c314-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c314-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c314-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c314-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c314-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c314-143">INPUTS</span></span>

## <span data-ttu-id="7c314-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c314-144">OUTPUTS</span></span>

### <span data-ttu-id="7c314-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7c314-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="7c314-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c314-146">NOTES</span></span>

<span data-ttu-id="7c314-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7c314-147">ALIASES</span></span>

## <span data-ttu-id="7c314-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c314-148">RELATED LINKS</span></span>

