---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207190"
---
# <span data-ttu-id="fda6c-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="fda6c-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="fda6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda6c-103">Létrehoz egy új MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="fda6c-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="fda6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fda6c-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fda6c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fda6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fda6c-106">Létrehoz egy új MariaDB-t.</span><span class="sxs-lookup"><span data-stu-id="fda6c-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="fda6c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fda6c-107">EXAMPLES</span></span>

### <span data-ttu-id="fda6c-108">1. példa: Új MariaDB létrehozása</span><span class="sxs-lookup"><span data-stu-id="fda6c-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="fda6c-109">Ez a parancs egy új MariaDB-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fda6c-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="fda6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fda6c-110">PARAMETERS</span></span>

### <span data-ttu-id="fda6c-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="fda6c-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="fda6c-112">A rendszergazdai jelszónak a SecureStringnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fda6c-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="fda6c-113">-AdministratorUsername</span></span>
<span data-ttu-id="fda6c-114">A rendszergazda felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="fda6c-114">Username of administrator.</span></span>

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

### <span data-ttu-id="fda6c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fda6c-115">-AsJob</span></span>
<span data-ttu-id="fda6c-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="fda6c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fda6c-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="fda6c-117">-BackupRetentionDay</span></span>
<span data-ttu-id="fda6c-118">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="fda6c-118">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda6c-119">-DefaultProfile</span></span>
<span data-ttu-id="fda6c-120">régió DefaultParameters Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fda6c-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda6c-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="fda6c-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="fda6c-122">Engedélyezze a georedundáns helymeghatározást, vagy ne engedélyezze a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="fda6c-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-123">-Location</span><span class="sxs-lookup"><span data-stu-id="fda6c-123">-Location</span></span>
<span data-ttu-id="fda6c-124">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="fda6c-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="fda6c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fda6c-125">-Name</span></span>
<span data-ttu-id="fda6c-126">A MariaDB-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fda6c-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="fda6c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fda6c-127">-NoWait</span></span>
<span data-ttu-id="fda6c-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="fda6c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fda6c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda6c-129">-ResourceGroupName</span></span>
<span data-ttu-id="fda6c-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fda6c-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="fda6c-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="fda6c-131">-Sku</span></span>
<span data-ttu-id="fda6c-132">A termékváltozat neve, általában tier + family + cores (szint + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="fda6c-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="fda6c-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="fda6c-133">-SslEnforcement</span></span>
<span data-ttu-id="fda6c-134">Engedélyezze az ssl kényszerítési funkcióját, vagy ne, amikor a kiszolgálóhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="fda6c-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="fda6c-135">-StorageAutogrow</span></span>
<span data-ttu-id="fda6c-136">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="fda6c-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="fda6c-137">-StorageInMb</span></span>
<span data-ttu-id="fda6c-138">A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="fda6c-138">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fda6c-139">-SubscriptionId</span></span>
<span data-ttu-id="fda6c-140">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része</span><span class="sxs-lookup"><span data-stu-id="fda6c-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="fda6c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="fda6c-141">-Tag</span></span>
<span data-ttu-id="fda6c-142">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="fda6c-142">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="fda6c-143">-Version</span></span>
<span data-ttu-id="fda6c-144">Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="fda6c-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fda6c-145">-Confirm</span></span>
<span data-ttu-id="fda6c-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fda6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda6c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda6c-147">-WhatIf</span></span>
<span data-ttu-id="fda6c-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fda6c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda6c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fda6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda6c-150">CommonParameters</span></span>
<span data-ttu-id="fda6c-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda6c-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fda6c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda6c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fda6c-153">INPUTS</span></span>

## <span data-ttu-id="fda6c-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fda6c-154">OUTPUTS</span></span>

### <span data-ttu-id="fda6c-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="fda6c-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="fda6c-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fda6c-156">NOTES</span></span>

<span data-ttu-id="fda6c-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fda6c-157">ALIASES</span></span>

## <span data-ttu-id="fda6c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fda6c-158">RELATED LINKS</span></span>

