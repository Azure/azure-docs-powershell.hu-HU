---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466357"
---
# <span data-ttu-id="22f41-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="22f41-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="22f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f41-102">SYNOPSIS</span></span>
<span data-ttu-id="22f41-103">A megadott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="22f41-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="22f41-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22f41-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22f41-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22f41-105">DESCRIPTION</span></span>
<span data-ttu-id="22f41-106">A megadott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="22f41-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="22f41-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22f41-107">EXAMPLES</span></span>

### <span data-ttu-id="22f41-108">1. példa: Az adott Kusto-fürt és adatbázis adatbázis-kezelőinek listája</span><span class="sxs-lookup"><span data-stu-id="22f41-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="22f41-109">A fenti parancs az adott Kusto-fürt és adatbázis adatbázis-kezelőinek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="22f41-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="22f41-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f41-110">PARAMETERS</span></span>

### <span data-ttu-id="22f41-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="22f41-111">-ClusterName</span></span>
<span data-ttu-id="22f41-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="22f41-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="22f41-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22f41-113">-DatabaseName</span></span>
<span data-ttu-id="22f41-114">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="22f41-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="22f41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f41-115">-DefaultProfile</span></span>
<span data-ttu-id="22f41-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22f41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22f41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f41-117">-ResourceGroupName</span></span>
<span data-ttu-id="22f41-118">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22f41-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="22f41-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22f41-119">-SubscriptionId</span></span>
<span data-ttu-id="22f41-120">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="22f41-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="22f41-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="22f41-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="22f41-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22f41-122">-Confirm</span></span>
<span data-ttu-id="22f41-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22f41-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f41-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f41-124">-WhatIf</span></span>
<span data-ttu-id="22f41-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22f41-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f41-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22f41-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f41-127">CommonParameters</span></span>
<span data-ttu-id="22f41-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f41-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22f41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f41-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22f41-130">INPUTS</span></span>

## <span data-ttu-id="22f41-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22f41-131">OUTPUTS</span></span>

### <span data-ttu-id="22f41-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="22f41-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="22f41-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22f41-133">NOTES</span></span>

<span data-ttu-id="22f41-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="22f41-134">ALIASES</span></span>

## <span data-ttu-id="22f41-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22f41-135">RELATED LINKS</span></span>

