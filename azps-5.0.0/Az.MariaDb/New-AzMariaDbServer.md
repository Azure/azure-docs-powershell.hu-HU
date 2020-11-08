---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194357"
---
# <span data-ttu-id="c8daf-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="c8daf-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="c8daf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8daf-102">SYNOPSIS</span></span>
<span data-ttu-id="c8daf-103">Új MariaDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8daf-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="c8daf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8daf-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8daf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8daf-105">DESCRIPTION</span></span>
<span data-ttu-id="c8daf-106">Új MariaDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8daf-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="c8daf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8daf-107">EXAMPLES</span></span>

### <span data-ttu-id="c8daf-108">Példa 1: új MariaDB létrehozása</span><span class="sxs-lookup"><span data-stu-id="c8daf-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="c8daf-109">A parancs új MariaDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8daf-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="c8daf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8daf-110">PARAMETERS</span></span>

### <span data-ttu-id="c8daf-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c8daf-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c8daf-112">A rendszergazda jelszava SecureString kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c8daf-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="c8daf-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="c8daf-113">-AdministratorUsername</span></span>
<span data-ttu-id="c8daf-114">A rendszergazda felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="c8daf-114">Username of administrator.</span></span>

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

### <span data-ttu-id="c8daf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8daf-115">-AsJob</span></span>
<span data-ttu-id="c8daf-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="c8daf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c8daf-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c8daf-117">-BackupRetentionDay</span></span>
<span data-ttu-id="c8daf-118">A kiszolgáló biztonságimásolat-adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="c8daf-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="c8daf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8daf-119">-DefaultProfile</span></span>
<span data-ttu-id="c8daf-120">terület: az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetések DefaultParameters.</span><span class="sxs-lookup"><span data-stu-id="c8daf-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8daf-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="c8daf-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="c8daf-122">Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="c8daf-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="c8daf-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="c8daf-123">-Location</span></span>
<span data-ttu-id="c8daf-124">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="c8daf-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c8daf-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8daf-125">-Name</span></span>
<span data-ttu-id="c8daf-126">MariaDB-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c8daf-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="c8daf-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="c8daf-127">-NoWait</span></span>
<span data-ttu-id="c8daf-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="c8daf-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c8daf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8daf-129">-ResourceGroupName</span></span>
<span data-ttu-id="c8daf-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8daf-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="c8daf-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8daf-131">-Sku</span></span>
<span data-ttu-id="c8daf-132">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c8daf-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c8daf-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c8daf-133">-SslEnforcement</span></span>
<span data-ttu-id="c8daf-134">Engedélyezze az SSL-kényszerítést, vagy ne a csatlakozás a kiszolgálóhoz lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c8daf-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="c8daf-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c8daf-135">-StorageAutogrow</span></span>
<span data-ttu-id="c8daf-136">A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c8daf-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="c8daf-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c8daf-137">-StorageInMb</span></span>
<span data-ttu-id="c8daf-138">Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c8daf-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="c8daf-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8daf-139">-SubscriptionId</span></span>
<span data-ttu-id="c8daf-140">Az előfizetési azonosító az összes szolgáltatási hívás URI-ja része</span><span class="sxs-lookup"><span data-stu-id="c8daf-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="c8daf-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="c8daf-141">-Tag</span></span>
<span data-ttu-id="c8daf-142">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="c8daf-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c8daf-143">-Verzió</span><span class="sxs-lookup"><span data-stu-id="c8daf-143">-Version</span></span>
<span data-ttu-id="c8daf-144">Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="c8daf-144">Server version.</span></span>

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

### <span data-ttu-id="c8daf-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8daf-145">-Confirm</span></span>
<span data-ttu-id="c8daf-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8daf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8daf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8daf-147">-WhatIf</span></span>
<span data-ttu-id="c8daf-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8daf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8daf-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8daf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8daf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8daf-150">CommonParameters</span></span>
<span data-ttu-id="c8daf-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8daf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8daf-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8daf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8daf-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8daf-153">INPUTS</span></span>

## <span data-ttu-id="c8daf-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8daf-154">OUTPUTS</span></span>

### <span data-ttu-id="c8daf-155">Microsoft. Azure. PowerShell. parancsmagok. MariaDb. modellek. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c8daf-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c8daf-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8daf-156">NOTES</span></span>

<span data-ttu-id="c8daf-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c8daf-157">ALIASES</span></span>

## <span data-ttu-id="c8daf-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8daf-158">RELATED LINKS</span></span>

