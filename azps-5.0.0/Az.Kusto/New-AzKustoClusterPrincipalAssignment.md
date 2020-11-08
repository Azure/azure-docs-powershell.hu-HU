---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194707"
---
# <span data-ttu-id="e50c4-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e50c4-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e50c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e50c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e50c4-103">Hozzon létre egy Kusto-fürtös principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e50c4-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e50c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e50c4-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e50c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e50c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e50c4-106">Hozzon létre egy Kusto-fürtös principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e50c4-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e50c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e50c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e50c4-108">Példa 1: Kusto-cluster principalAssignment létrehozása</span><span class="sxs-lookup"><span data-stu-id="e50c4-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="e50c4-109">A fenti parancs Kusto-fürtöt hoz létre principalAssignment</span><span class="sxs-lookup"><span data-stu-id="e50c4-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="e50c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e50c4-110">PARAMETERS</span></span>

### <span data-ttu-id="e50c4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e50c4-111">-AsJob</span></span>
<span data-ttu-id="e50c4-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e50c4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e50c4-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e50c4-113">-ClusterName</span></span>
<span data-ttu-id="e50c4-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e50c4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e50c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50c4-115">-DefaultProfile</span></span>
<span data-ttu-id="e50c4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e50c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e50c4-117">-Várva</span><span class="sxs-lookup"><span data-stu-id="e50c4-117">-NoWait</span></span>
<span data-ttu-id="e50c4-118">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e50c4-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e50c4-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e50c4-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="e50c4-120">A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="e50c4-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="e50c4-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="e50c4-121">-PrincipalId</span></span>
<span data-ttu-id="e50c4-122">A cluster Principal-hoz rendelt fő azonosító.</span><span class="sxs-lookup"><span data-stu-id="e50c4-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="e50c4-123">Lehet felhasználói e-mail-cím, alkalmazásspecifikus azonosító vagy biztonsági csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e50c4-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="e50c4-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="e50c4-124">-PrincipalType</span></span>
<span data-ttu-id="e50c4-125">Fő típus.</span><span class="sxs-lookup"><span data-stu-id="e50c4-125">Principal type.</span></span>

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

### <span data-ttu-id="e50c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="e50c4-127">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e50c4-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e50c4-128">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="e50c4-128">-Role</span></span>
<span data-ttu-id="e50c4-129">A cluster Principal szerepkör</span><span class="sxs-lookup"><span data-stu-id="e50c4-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="e50c4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e50c4-130">-SubscriptionId</span></span>
<span data-ttu-id="e50c4-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e50c4-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e50c4-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e50c4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e50c4-133">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="e50c4-133">-TenantId</span></span>
<span data-ttu-id="e50c4-134">A megbízó bérlői azonosítója</span><span class="sxs-lookup"><span data-stu-id="e50c4-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="e50c4-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e50c4-135">-Confirm</span></span>
<span data-ttu-id="e50c4-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e50c4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50c4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50c4-137">-WhatIf</span></span>
<span data-ttu-id="e50c4-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e50c4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50c4-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e50c4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e50c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50c4-140">CommonParameters</span></span>
<span data-ttu-id="e50c4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e50c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50c4-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e50c4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50c4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e50c4-143">INPUTS</span></span>

## <span data-ttu-id="e50c4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e50c4-144">OUTPUTS</span></span>

### <span data-ttu-id="e50c4-145">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e50c4-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e50c4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e50c4-146">NOTES</span></span>

<span data-ttu-id="e50c4-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e50c4-147">ALIASES</span></span>

## <span data-ttu-id="e50c4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e50c4-148">RELATED LINKS</span></span>
