---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927961"
---
# <span data-ttu-id="b40a8-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b40a8-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="b40a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b40a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b40a8-103">Kusto-fürtadatbázis-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b40a8-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="b40a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b40a8-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b40a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b40a8-105">DESCRIPTION</span></span>
<span data-ttu-id="b40a8-106">Kusto-fürtadatbázis-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b40a8-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="b40a8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b40a8-107">EXAMPLES</span></span>

### <span data-ttu-id="b40a8-108">1. példa: Kusto-fürtadatbázis-egyszerű hozzárendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="b40a8-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="b40a8-109">A fenti parancs létrehoz egy Kusto-fürtadatbázis-hozzárendelést</span><span class="sxs-lookup"><span data-stu-id="b40a8-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="b40a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b40a8-110">PARAMETERS</span></span>

### <span data-ttu-id="b40a8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b40a8-111">-AsJob</span></span>
<span data-ttu-id="b40a8-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b40a8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b40a8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b40a8-113">-ClusterName</span></span>
<span data-ttu-id="b40a8-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b40a8-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b40a8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b40a8-115">-DatabaseName</span></span>
<span data-ttu-id="b40a8-116">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b40a8-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b40a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40a8-117">-DefaultProfile</span></span>
<span data-ttu-id="b40a8-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b40a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b40a8-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b40a8-119">-NoWait</span></span>
<span data-ttu-id="b40a8-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b40a8-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b40a8-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b40a8-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b40a8-122">A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="b40a8-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="b40a8-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="b40a8-123">-PrincipalId</span></span>
<span data-ttu-id="b40a8-124">Az adatbázis-egyszerűhöz rendelt elsődleges azonosító.</span><span class="sxs-lookup"><span data-stu-id="b40a8-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="b40a8-125">Ez lehet egy felhasználói e-mail-cím, alkalmazásazonosító vagy biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b40a8-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="b40a8-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="b40a8-126">-PrincipalType</span></span>
<span data-ttu-id="b40a8-127">Egyszerű típus.</span><span class="sxs-lookup"><span data-stu-id="b40a8-127">Principal type.</span></span>

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

### <span data-ttu-id="b40a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="b40a8-129">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b40a8-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b40a8-130">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="b40a8-130">-Role</span></span>
<span data-ttu-id="b40a8-131">Az adatbázis elsődleges szerepköre.</span><span class="sxs-lookup"><span data-stu-id="b40a8-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40a8-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b40a8-132">-SubscriptionId</span></span>
<span data-ttu-id="b40a8-133">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b40a8-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b40a8-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b40a8-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b40a8-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b40a8-135">-TenantId</span></span>
<span data-ttu-id="b40a8-136">A tőkenév bérlőazonosítója</span><span class="sxs-lookup"><span data-stu-id="b40a8-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="b40a8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b40a8-137">-Confirm</span></span>
<span data-ttu-id="b40a8-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b40a8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b40a8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40a8-139">-WhatIf</span></span>
<span data-ttu-id="b40a8-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b40a8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b40a8-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b40a8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b40a8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40a8-142">CommonParameters</span></span>
<span data-ttu-id="b40a8-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40a8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40a8-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b40a8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40a8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b40a8-145">INPUTS</span></span>

## <span data-ttu-id="b40a8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b40a8-146">OUTPUTS</span></span>

### <span data-ttu-id="b40a8-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b40a8-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="b40a8-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b40a8-148">NOTES</span></span>

<span data-ttu-id="b40a8-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b40a8-149">ALIASES</span></span>

## <span data-ttu-id="b40a8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b40a8-150">RELATED LINKS</span></span>

