---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152458"
---
# <span data-ttu-id="159e5-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="159e5-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="159e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="159e5-102">SYNOPSIS</span></span>
<span data-ttu-id="159e5-103">A megadott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="159e5-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="159e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="159e5-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="159e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="159e5-105">DESCRIPTION</span></span>
<span data-ttu-id="159e5-106">A megadott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="159e5-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="159e5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="159e5-107">EXAMPLES</span></span>

### <span data-ttu-id="159e5-108">1. példa: Az adott Kusto-fürt és adatbázis adatbázis-kezelőinek listája</span><span class="sxs-lookup"><span data-stu-id="159e5-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="159e5-109">A fenti parancs az adott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="159e5-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="159e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="159e5-110">PARAMETERS</span></span>

### <span data-ttu-id="159e5-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="159e5-111">-ClusterName</span></span>
<span data-ttu-id="159e5-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="159e5-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="159e5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="159e5-113">-DatabaseName</span></span>
<span data-ttu-id="159e5-114">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="159e5-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="159e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159e5-115">-DefaultProfile</span></span>
<span data-ttu-id="159e5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="159e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="159e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="159e5-118">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="159e5-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="159e5-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="159e5-119">-SubscriptionId</span></span>
<span data-ttu-id="159e5-120">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="159e5-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="159e5-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="159e5-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159e5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="159e5-122">-Confirm</span></span>
<span data-ttu-id="159e5-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="159e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="159e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="159e5-124">-WhatIf</span></span>
<span data-ttu-id="159e5-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="159e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="159e5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="159e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="159e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159e5-127">CommonParameters</span></span>
<span data-ttu-id="159e5-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159e5-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="159e5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159e5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="159e5-130">INPUTS</span></span>

## <span data-ttu-id="159e5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="159e5-131">OUTPUTS</span></span>

### <span data-ttu-id="159e5-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="159e5-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="159e5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="159e5-133">NOTES</span></span>

<span data-ttu-id="159e5-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="159e5-134">ALIASES</span></span>

## <span data-ttu-id="159e5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="159e5-135">RELATED LINKS</span></span>

