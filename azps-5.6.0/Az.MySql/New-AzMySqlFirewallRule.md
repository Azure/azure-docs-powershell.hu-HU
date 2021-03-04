---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 84c5e5e49d80c04bcbfe3f7ec72e018ac7984bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921946"
---
# <span data-ttu-id="c234b-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c234b-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c234b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c234b-102">SYNOPSIS</span></span>
<span data-ttu-id="c234b-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c234b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c234b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c234b-104">SYNTAX</span></span>

### <span data-ttu-id="c234b-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c234b-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c234b-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="c234b-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c234b-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c234b-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c234b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c234b-108">DESCRIPTION</span></span>
<span data-ttu-id="c234b-109">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c234b-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c234b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c234b-110">EXAMPLES</span></span>

### <span data-ttu-id="c234b-111">1. példa: Új MySql-kiszolgáló tűzfalszabályának létrehozása</span><span class="sxs-lookup"><span data-stu-id="c234b-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="c234b-112">Ez a parancsmag mySql-kiszolgáló tűzfalszabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c234b-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="c234b-113">2. példa: Új MySql tűzfalszabály létrehozása a -ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="c234b-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="c234b-114">Ezek a parancsmagok mySql tűzfalszabályt hoznak létre a -ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="c234b-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="c234b-115">3. példa: Új MySql tűzfalszabály létrehozása az összes IP-kód engedélyezése érdekében</span><span class="sxs-lookup"><span data-stu-id="c234b-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="c234b-116">Ezek a parancsmagok új MySql tűzfalszabályt hoznak létre, amely engedélyezi az összes IP-et.</span><span class="sxs-lookup"><span data-stu-id="c234b-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="c234b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c234b-117">PARAMETERS</span></span>

### <span data-ttu-id="c234b-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="c234b-118">-AllowAll</span></span>
<span data-ttu-id="c234b-119">A 0.0.0.0-tól a 255.255.255.255.255-ig.</span><span class="sxs-lookup"><span data-stu-id="c234b-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="c234b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c234b-120">-AsJob</span></span>
<span data-ttu-id="c234b-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="c234b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c234b-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c234b-122">-ClientIPAddress</span></span>
<span data-ttu-id="c234b-123">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c234b-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c234b-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c234b-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c234b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c234b-125">-DefaultProfile</span></span>
<span data-ttu-id="c234b-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c234b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c234b-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c234b-127">-EndIPAddress</span></span>
<span data-ttu-id="c234b-128">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c234b-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c234b-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c234b-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c234b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c234b-130">-Name</span></span>
<span data-ttu-id="c234b-131">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c234b-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="c234b-132">Ha nincs megadva, az alapértelmezett érték nincs meghatározva.</span><span class="sxs-lookup"><span data-stu-id="c234b-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="c234b-133">Ha az AllowAll is jelen van, az alapértelmezett AllowAll_yyyy-MM-dd_HH-mm-mm.</span><span class="sxs-lookup"><span data-stu-id="c234b-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="c234b-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c234b-134">-NoWait</span></span>
<span data-ttu-id="c234b-135">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="c234b-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c234b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c234b-136">-ResourceGroupName</span></span>
<span data-ttu-id="c234b-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c234b-137">The name of the resource group.</span></span>
<span data-ttu-id="c234b-138">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c234b-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c234b-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c234b-139">-ServerName</span></span>
<span data-ttu-id="c234b-140">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c234b-140">The name of the server.</span></span>

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

### <span data-ttu-id="c234b-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c234b-141">-StartIPAddress</span></span>
<span data-ttu-id="c234b-142">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c234b-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c234b-143">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c234b-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c234b-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c234b-144">-SubscriptionId</span></span>
<span data-ttu-id="c234b-145">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c234b-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c234b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c234b-146">-Confirm</span></span>
<span data-ttu-id="c234b-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c234b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c234b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c234b-148">-WhatIf</span></span>
<span data-ttu-id="c234b-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c234b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c234b-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c234b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c234b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c234b-151">CommonParameters</span></span>
<span data-ttu-id="c234b-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c234b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c234b-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c234b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c234b-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c234b-154">INPUTS</span></span>

## <span data-ttu-id="c234b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c234b-155">OUTPUTS</span></span>

### <span data-ttu-id="c234b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c234b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c234b-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c234b-157">NOTES</span></span>

<span data-ttu-id="c234b-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c234b-158">ALIASES</span></span>

## <span data-ttu-id="c234b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c234b-159">RELATED LINKS</span></span>

