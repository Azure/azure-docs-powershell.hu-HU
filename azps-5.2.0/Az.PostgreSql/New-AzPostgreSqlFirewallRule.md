---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358818"
---
# <span data-ttu-id="45a0f-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45a0f-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="45a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="45a0f-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="45a0f-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="45a0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45a0f-104">SYNTAX</span></span>

### <span data-ttu-id="45a0f-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45a0f-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45a0f-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="45a0f-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="45a0f-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="45a0f-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45a0f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45a0f-108">DESCRIPTION</span></span>
<span data-ttu-id="45a0f-109">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="45a0f-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="45a0f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45a0f-110">EXAMPLES</span></span>

### <span data-ttu-id="45a0f-111">1. példa: Új PostgreSql-kiszolgáló tűzfalszabályának létrehozása</span><span class="sxs-lookup"><span data-stu-id="45a0f-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="45a0f-112">Ezek a parancsmagok PostgreSql-kiszolgáló tűzfalszabályt hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="45a0f-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="45a0f-113">2. példa: Új PostgreSql tűzfalszabály létrehozása a -ClientIPAddress segítségével.</span><span class="sxs-lookup"><span data-stu-id="45a0f-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="45a0f-114">Ez a parancsmag létrehoz egy PostgreSql tűzfalszabályt a -ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="45a0f-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="45a0f-115">3. példa: Új PostgreSql tűzfalszabály létrehozása az összes IP-kód engedélyezése érdekében</span><span class="sxs-lookup"><span data-stu-id="45a0f-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="45a0f-116">Ez a parancsmag egy új PostgreSql tűzfalszabályt hoz létre, amely engedélyezi az összes IP-et.</span><span class="sxs-lookup"><span data-stu-id="45a0f-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="45a0f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45a0f-117">PARAMETERS</span></span>

### <span data-ttu-id="45a0f-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="45a0f-118">-AllowAll</span></span>
<span data-ttu-id="45a0f-119">A 0.0.0.0-tól a 255.255.255.255.255-ig.</span><span class="sxs-lookup"><span data-stu-id="45a0f-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a0f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45a0f-120">-AsJob</span></span>
<span data-ttu-id="45a0f-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="45a0f-121">Run the command as a job</span></span>

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

### <span data-ttu-id="45a0f-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="45a0f-122">-ClientIPAddress</span></span>
<span data-ttu-id="45a0f-123">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45a0f-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="45a0f-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="45a0f-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a0f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a0f-125">-DefaultProfile</span></span>
<span data-ttu-id="45a0f-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45a0f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45a0f-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="45a0f-127">-EndIPAddress</span></span>
<span data-ttu-id="45a0f-128">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="45a0f-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="45a0f-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="45a0f-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a0f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="45a0f-130">-Name</span></span>
<span data-ttu-id="45a0f-131">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="45a0f-131">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a0f-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45a0f-132">-NoWait</span></span>
<span data-ttu-id="45a0f-133">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="45a0f-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45a0f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a0f-134">-ResourceGroupName</span></span>
<span data-ttu-id="45a0f-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="45a0f-135">The name of the resource group.</span></span>
<span data-ttu-id="45a0f-136">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="45a0f-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45a0f-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45a0f-137">-ServerName</span></span>
<span data-ttu-id="45a0f-138">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="45a0f-138">The name of the server.</span></span>

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

### <span data-ttu-id="45a0f-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="45a0f-139">-StartIPAddress</span></span>
<span data-ttu-id="45a0f-140">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="45a0f-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="45a0f-141">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="45a0f-141">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a0f-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45a0f-142">-SubscriptionId</span></span>
<span data-ttu-id="45a0f-143">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45a0f-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45a0f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45a0f-144">-Confirm</span></span>
<span data-ttu-id="45a0f-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="45a0f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a0f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a0f-146">-WhatIf</span></span>
<span data-ttu-id="45a0f-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="45a0f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45a0f-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45a0f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a0f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a0f-149">CommonParameters</span></span>
<span data-ttu-id="45a0f-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a0f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a0f-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45a0f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a0f-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45a0f-152">INPUTS</span></span>

## <span data-ttu-id="45a0f-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45a0f-153">OUTPUTS</span></span>

### <span data-ttu-id="45a0f-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45a0f-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="45a0f-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45a0f-155">NOTES</span></span>

<span data-ttu-id="45a0f-156">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="45a0f-156">ALIASES</span></span>

## <span data-ttu-id="45a0f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45a0f-157">RELATED LINKS</span></span>

