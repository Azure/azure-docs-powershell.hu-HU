---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329499"
---
# <span data-ttu-id="6c042-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="6c042-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="6c042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c042-102">SYNOPSIS</span></span>
<span data-ttu-id="6c042-103">Új rugalmas MySQL-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="6c042-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="6c042-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c042-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c042-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c042-105">DESCRIPTION</span></span>
<span data-ttu-id="6c042-106">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="6c042-106">Creates a new server.</span></span>

## <span data-ttu-id="6c042-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c042-107">EXAMPLES</span></span>

### <span data-ttu-id="6c042-108">1. példa: Új rugalmas MySql-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="6c042-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="6c042-109">2. példa: Új, rugalmas MySql-kiszolgáló létrehozása alapértelmezett beállítással</span><span class="sxs-lookup"><span data-stu-id="6c042-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="6c042-110">MySql-kiszolgáló létrehozása alapértelmezett értékekkel.</span><span class="sxs-lookup"><span data-stu-id="6c042-110">Create MySql server with default values.</span></span>
<span data-ttu-id="6c042-111">A hely alapértelmezett értékei a 2. nyugat-amerikai régió, a termékváltozat Standard_B1ms, a termékváltozatréteg sivár, a tárterület mérete pedig 10GiB.</span><span class="sxs-lookup"><span data-stu-id="6c042-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="6c042-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c042-112">PARAMETERS</span></span>

### <span data-ttu-id="6c042-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6c042-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6c042-114">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="6c042-114">The password of the administrator.</span></span>
<span data-ttu-id="6c042-115">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="6c042-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="6c042-116">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="6c042-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="6c042-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="6c042-117">-AdministratorUserName</span></span>
<span data-ttu-id="6c042-118">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6c042-118">Administrator username for the server.</span></span>
<span data-ttu-id="6c042-119">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="6c042-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="6c042-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c042-120">-AsJob</span></span>
<span data-ttu-id="6c042-121">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="6c042-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="6c042-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6c042-122">-BackupRetentionDay</span></span>
<span data-ttu-id="6c042-123">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="6c042-123">Backup retention days for the server.</span></span>
<span data-ttu-id="6c042-124">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="6c042-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6c042-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c042-125">-DefaultProfile</span></span>
<span data-ttu-id="6c042-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c042-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c042-127">-Location</span><span class="sxs-lookup"><span data-stu-id="6c042-127">-Location</span></span>
<span data-ttu-id="6c042-128">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="6c042-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6c042-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6c042-129">-Name</span></span>
<span data-ttu-id="6c042-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6c042-130">The name of the server.</span></span>

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

### <span data-ttu-id="6c042-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6c042-131">-NoWait</span></span>
<span data-ttu-id="6c042-132">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="6c042-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6c042-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c042-133">-ResourceGroupName</span></span>
<span data-ttu-id="6c042-134">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="6c042-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6c042-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="6c042-135">-Sku</span></span>
<span data-ttu-id="6c042-136">A termékváltozat neve, jellemzően tier + family + cores (szint + családi + cores) (például Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="6c042-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="6c042-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6c042-137">-SkuTier</span></span>
<span data-ttu-id="6c042-138">A kiszolgáló számítási rétege.</span><span class="sxs-lookup"><span data-stu-id="6c042-138">Compute tier of the server.</span></span>
<span data-ttu-id="6c042-139">Elfogadott értékek: Sorozatos, GeneralPurpose, Memória optimalizálva.</span><span class="sxs-lookup"><span data-stu-id="6c042-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="6c042-140">Alapérték: Törhető.</span><span class="sxs-lookup"><span data-stu-id="6c042-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="6c042-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6c042-141">-StorageInMb</span></span>
<span data-ttu-id="6c042-142">A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="6c042-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6c042-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c042-143">-SubscriptionId</span></span>
<span data-ttu-id="6c042-144">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="6c042-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6c042-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c042-145">-Tag</span></span>
<span data-ttu-id="6c042-146">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="6c042-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6c042-147">-Version</span><span class="sxs-lookup"><span data-stu-id="6c042-147">-Version</span></span>
<span data-ttu-id="6c042-148">Kiszolgálói verzió.</span><span class="sxs-lookup"><span data-stu-id="6c042-148">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c042-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c042-149">-Confirm</span></span>
<span data-ttu-id="6c042-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6c042-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c042-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c042-151">-WhatIf</span></span>
<span data-ttu-id="6c042-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6c042-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c042-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c042-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c042-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c042-154">CommonParameters</span></span>
<span data-ttu-id="6c042-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c042-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c042-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c042-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c042-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c042-157">INPUTS</span></span>

## <span data-ttu-id="6c042-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c042-158">OUTPUTS</span></span>

### <span data-ttu-id="6c042-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6c042-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="6c042-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c042-160">NOTES</span></span>

<span data-ttu-id="6c042-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6c042-161">ALIASES</span></span>

## <span data-ttu-id="6c042-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c042-162">RELATED LINKS</span></span>

