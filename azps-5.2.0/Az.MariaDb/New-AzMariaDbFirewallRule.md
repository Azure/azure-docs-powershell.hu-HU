---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370325"
---
# <span data-ttu-id="c4a00-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4a00-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="c4a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a00-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a00-103">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c4a00-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c4a00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4a00-104">SYNTAX</span></span>

### <span data-ttu-id="c4a00-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4a00-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4a00-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="c4a00-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c4a00-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4a00-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4a00-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4a00-108">DESCRIPTION</span></span>
<span data-ttu-id="c4a00-109">Új tűzfalszabályt hoz létre, vagy frissíti a meglévő tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="c4a00-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c4a00-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4a00-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a00-111">1. példa: Tűzfalszabály létrehozása a MariaDB csoportban</span><span class="sxs-lookup"><span data-stu-id="c4a00-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="c4a00-112">Ez a parancs tűzfalszabályt hoz létre a MariaDB alatt.</span><span class="sxs-lookup"><span data-stu-id="c4a00-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="c4a00-113">2. példa: Új MariaDB tűzfalszabály létrehozása a -ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="c4a00-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="c4a00-114">Ez a parancsmag létrehoz egy MariaDB tűzfalszabályt a -ClientIPAddress használatával.</span><span class="sxs-lookup"><span data-stu-id="c4a00-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="c4a00-115">3. példa: Új MariaDB tűzfalszabály létrehozása az összes IP-fiók engedélyezése érdekében</span><span class="sxs-lookup"><span data-stu-id="c4a00-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="c4a00-116">Ez a parancsmag létrehoz egy új MariaDB tűzfalszabályt, amely engedélyezi az összes IP-et.</span><span class="sxs-lookup"><span data-stu-id="c4a00-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="c4a00-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4a00-117">PARAMETERS</span></span>

### <span data-ttu-id="c4a00-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="c4a00-118">-AllowAll</span></span>
<span data-ttu-id="c4a00-119">A 0.0.0.0-tól a 255.255.255.255.255-ig.</span><span class="sxs-lookup"><span data-stu-id="c4a00-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="c4a00-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4a00-120">-AsJob</span></span>
<span data-ttu-id="c4a00-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="c4a00-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c4a00-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4a00-122">-ClientIPAddress</span></span>
<span data-ttu-id="c4a00-123">Az ügyfél a kiszolgáló tűzfalszabályának egyetlen IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4a00-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c4a00-124">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4a00-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4a00-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a00-125">-DefaultProfile</span></span>
<span data-ttu-id="c4a00-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4a00-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a00-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4a00-127">-EndIPAddress</span></span>
<span data-ttu-id="c4a00-128">A kiszolgáló tűzfalszabályának záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4a00-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c4a00-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4a00-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4a00-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a00-130">-Name</span></span>
<span data-ttu-id="c4a00-131">A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c4a00-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="c4a00-132">Ha nincs megadva, az alapértelmezett érték nincs meghatározva.</span><span class="sxs-lookup"><span data-stu-id="c4a00-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="c4a00-133">Ha az AllowAll érték meg van jelölve, az alapértelmezett AllowAll_yyyy-MM-dd_HH-mm-mm.</span><span class="sxs-lookup"><span data-stu-id="c4a00-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="c4a00-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4a00-134">-NoWait</span></span>
<span data-ttu-id="c4a00-135">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="c4a00-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4a00-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a00-136">-ResourceGroupName</span></span>
<span data-ttu-id="c4a00-137">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4a00-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c4a00-138">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="c4a00-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c4a00-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4a00-139">-ServerName</span></span>
<span data-ttu-id="c4a00-140">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c4a00-140">The name of the server.</span></span>

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

### <span data-ttu-id="c4a00-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4a00-141">-StartIPAddress</span></span>
<span data-ttu-id="c4a00-142">A kiszolgáló tűzfalszabályának kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4a00-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c4a00-143">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c4a00-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c4a00-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4a00-144">-SubscriptionId</span></span>
<span data-ttu-id="c4a00-145">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="c4a00-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c4a00-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a00-146">-Confirm</span></span>
<span data-ttu-id="c4a00-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4a00-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a00-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a00-148">-WhatIf</span></span>
<span data-ttu-id="c4a00-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4a00-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a00-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4a00-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a00-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a00-151">CommonParameters</span></span>
<span data-ttu-id="c4a00-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a00-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a00-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4a00-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a00-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4a00-154">INPUTS</span></span>

## <span data-ttu-id="c4a00-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a00-155">OUTPUTS</span></span>

### <span data-ttu-id="c4a00-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4a00-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="c4a00-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4a00-157">NOTES</span></span>

<span data-ttu-id="c4a00-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c4a00-158">ALIASES</span></span>

## <span data-ttu-id="c4a00-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4a00-159">RELATED LINKS</span></span>

