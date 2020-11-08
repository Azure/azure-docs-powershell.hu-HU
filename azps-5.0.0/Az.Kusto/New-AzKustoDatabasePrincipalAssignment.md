---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194701"
---
# <span data-ttu-id="47642-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="47642-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="47642-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47642-102">SYNOPSIS</span></span>
<span data-ttu-id="47642-103">Létrehoz egy Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="47642-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="47642-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47642-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47642-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47642-105">DESCRIPTION</span></span>
<span data-ttu-id="47642-106">Létrehoz egy Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="47642-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="47642-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47642-107">EXAMPLES</span></span>

### <span data-ttu-id="47642-108">1. példa: Kusto-cluster Database principalAssignment létrehozása</span><span class="sxs-lookup"><span data-stu-id="47642-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="47642-109">A fenti parancs létrehoz egy Kusto-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="47642-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="47642-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47642-110">PARAMETERS</span></span>

### <span data-ttu-id="47642-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47642-111">-AsJob</span></span>
<span data-ttu-id="47642-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="47642-112">Run the command as a job</span></span>

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

### <span data-ttu-id="47642-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="47642-113">-ClusterName</span></span>
<span data-ttu-id="47642-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="47642-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="47642-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47642-115">-DatabaseName</span></span>
<span data-ttu-id="47642-116">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="47642-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="47642-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47642-117">-DefaultProfile</span></span>
<span data-ttu-id="47642-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47642-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47642-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="47642-119">-NoWait</span></span>
<span data-ttu-id="47642-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="47642-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47642-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="47642-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="47642-122">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="47642-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="47642-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="47642-123">-PrincipalId</span></span>
<span data-ttu-id="47642-124">Az adatbázis-megbízóhoz rendelt fő azonosító.</span><span class="sxs-lookup"><span data-stu-id="47642-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="47642-125">Lehet felhasználói e-mail-cím, alkalmazásspecifikus azonosító vagy biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="47642-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="47642-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="47642-126">-PrincipalType</span></span>
<span data-ttu-id="47642-127">Fő típus.</span><span class="sxs-lookup"><span data-stu-id="47642-127">Principal type.</span></span>

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

### <span data-ttu-id="47642-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47642-128">-ResourceGroupName</span></span>
<span data-ttu-id="47642-129">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47642-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="47642-130">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="47642-130">-Role</span></span>
<span data-ttu-id="47642-131">Adatbázis-fő szerepkör</span><span class="sxs-lookup"><span data-stu-id="47642-131">Database principal role.</span></span>

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

### <span data-ttu-id="47642-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47642-132">-SubscriptionId</span></span>
<span data-ttu-id="47642-133">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="47642-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47642-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="47642-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47642-135">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="47642-135">-TenantId</span></span>
<span data-ttu-id="47642-136">A megbízó bérlői azonosítója</span><span class="sxs-lookup"><span data-stu-id="47642-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="47642-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47642-137">-Confirm</span></span>
<span data-ttu-id="47642-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47642-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47642-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47642-139">-WhatIf</span></span>
<span data-ttu-id="47642-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47642-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47642-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47642-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47642-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47642-142">CommonParameters</span></span>
<span data-ttu-id="47642-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47642-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47642-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47642-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47642-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47642-145">INPUTS</span></span>

## <span data-ttu-id="47642-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47642-146">OUTPUTS</span></span>

### <span data-ttu-id="47642-147">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="47642-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="47642-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47642-148">NOTES</span></span>

<span data-ttu-id="47642-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="47642-149">ALIASES</span></span>

## <span data-ttu-id="47642-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47642-150">RELATED LINKS</span></span>

