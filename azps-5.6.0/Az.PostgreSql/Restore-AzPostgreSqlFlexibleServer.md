---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919417"
---
# <span data-ttu-id="95e40-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="95e40-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="95e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e40-102">SYNOPSIS</span></span>
<span data-ttu-id="95e40-103">Rugalmas PostgreSQL-kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="95e40-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="95e40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95e40-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95e40-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95e40-105">DESCRIPTION</span></span>
<span data-ttu-id="95e40-106">Kiszolgáló visszaállítása meglévő biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="95e40-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="95e40-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95e40-107">EXAMPLES</span></span>

### <span data-ttu-id="95e40-108">1. példa: PostgreSql-kiszolgáló visszaállítása a PointInTime restore használatával</span><span class="sxs-lookup"><span data-stu-id="95e40-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="95e40-109">Ezek a parancsmagok a PointInTime restore segítségével visszaállítják a PostgreSql-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="95e40-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="95e40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95e40-110">PARAMETERS</span></span>

### <span data-ttu-id="95e40-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95e40-111">-AsJob</span></span>
<span data-ttu-id="95e40-112">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="95e40-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="95e40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e40-113">-DefaultProfile</span></span>
<span data-ttu-id="95e40-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95e40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e40-115">-Location</span><span class="sxs-lookup"><span data-stu-id="95e40-115">-Location</span></span>
<span data-ttu-id="95e40-116">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="95e40-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="95e40-117">-Name</span><span class="sxs-lookup"><span data-stu-id="95e40-117">-Name</span></span>
<span data-ttu-id="95e40-118">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="95e40-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e40-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95e40-119">-NoWait</span></span>
<span data-ttu-id="95e40-120">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="95e40-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="95e40-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e40-121">-ResourceGroupName</span></span>
<span data-ttu-id="95e40-122">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="95e40-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="95e40-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="95e40-123">-RestorePointInTime</span></span>
<span data-ttu-id="95e40-124">A visszaállítás ideje (ISO8601 formátum), például 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="95e40-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e40-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="95e40-125">-SourceServerName</span></span>
<span data-ttu-id="95e40-126">A forráskiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="95e40-126">The name of the source server.</span></span>

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

### <span data-ttu-id="95e40-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95e40-127">-SubscriptionId</span></span>
<span data-ttu-id="95e40-128">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="95e40-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="95e40-129">-Zone</span><span class="sxs-lookup"><span data-stu-id="95e40-129">-Zone</span></span>
<span data-ttu-id="95e40-130">Elérhetőségi zóna, amelybe ki kellépítenünk az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="95e40-130">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="95e40-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95e40-131">-Confirm</span></span>
<span data-ttu-id="95e40-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95e40-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e40-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e40-133">-WhatIf</span></span>
<span data-ttu-id="95e40-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95e40-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e40-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95e40-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e40-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e40-136">CommonParameters</span></span>
<span data-ttu-id="95e40-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e40-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e40-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95e40-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e40-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95e40-139">INPUTS</span></span>

## <span data-ttu-id="95e40-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95e40-140">OUTPUTS</span></span>

### <span data-ttu-id="95e40-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="95e40-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="95e40-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95e40-142">NOTES</span></span>

<span data-ttu-id="95e40-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="95e40-143">ALIASES</span></span>

## <span data-ttu-id="95e40-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95e40-144">RELATED LINKS</span></span>

