---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 683ca81587ff7c71f1406eb7a4accef37aac794d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466289"
---
# <span data-ttu-id="1fe49-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="1fe49-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="1fe49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe49-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe49-103">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1fe49-103">Creates a new server.</span></span>

## <span data-ttu-id="1fe49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fe49-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fe49-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fe49-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe49-106">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1fe49-106">Creates a new server.</span></span>

## <span data-ttu-id="1fe49-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fe49-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe49-108">1. példa: Új MySql-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="1fe49-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="1fe49-109">Ezek a parancsmagok új MySql-kiszolgálót hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="1fe49-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="1fe49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe49-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe49-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1fe49-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1fe49-112">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="1fe49-112">The password of the administrator.</span></span>
<span data-ttu-id="1fe49-113">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="1fe49-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="1fe49-114">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="1fe49-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="1fe49-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="1fe49-115">-AdministratorUserName</span></span>
<span data-ttu-id="1fe49-116">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="1fe49-116">Administrator username for the server.</span></span>
<span data-ttu-id="1fe49-117">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="1fe49-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="1fe49-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fe49-118">-AsJob</span></span>
<span data-ttu-id="1fe49-119">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="1fe49-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="1fe49-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="1fe49-120">-BackupRetentionDay</span></span>
<span data-ttu-id="1fe49-121">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="1fe49-121">Backup retention days for the server.</span></span>
<span data-ttu-id="1fe49-122">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="1fe49-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="1fe49-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe49-123">-DefaultProfile</span></span>
<span data-ttu-id="1fe49-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fe49-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe49-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="1fe49-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="1fe49-126">Engedélyezze a georedundáns helymeghatározást, vagy ne engedélyezze a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="1fe49-126">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe49-127">-Location</span><span class="sxs-lookup"><span data-stu-id="1fe49-127">-Location</span></span>
<span data-ttu-id="1fe49-128">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="1fe49-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1fe49-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1fe49-129">-Name</span></span>
<span data-ttu-id="1fe49-130">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1fe49-130">The name of the server.</span></span>

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

### <span data-ttu-id="1fe49-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fe49-131">-NoWait</span></span>
<span data-ttu-id="1fe49-132">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="1fe49-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="1fe49-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe49-133">-ResourceGroupName</span></span>
<span data-ttu-id="1fe49-134">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="1fe49-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1fe49-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="1fe49-135">-Sku</span></span>
<span data-ttu-id="1fe49-136">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1fe49-136">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="1fe49-137">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="1fe49-137">-SslEnforcement</span></span>
<span data-ttu-id="1fe49-138">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="1fe49-138">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe49-139">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="1fe49-139">-StorageAutogrow</span></span>
<span data-ttu-id="1fe49-140">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="1fe49-140">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe49-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="1fe49-141">-StorageInMb</span></span>
<span data-ttu-id="1fe49-142">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="1fe49-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="1fe49-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fe49-143">-SubscriptionId</span></span>
<span data-ttu-id="1fe49-144">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="1fe49-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="1fe49-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fe49-145">-Tag</span></span>
<span data-ttu-id="1fe49-146">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="1fe49-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1fe49-147">-Version</span><span class="sxs-lookup"><span data-stu-id="1fe49-147">-Version</span></span>
<span data-ttu-id="1fe49-148">Kiszolgálói verzió.</span><span class="sxs-lookup"><span data-stu-id="1fe49-148">Server version.</span></span>

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

### <span data-ttu-id="1fe49-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe49-149">-Confirm</span></span>
<span data-ttu-id="1fe49-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1fe49-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe49-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe49-151">-WhatIf</span></span>
<span data-ttu-id="1fe49-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1fe49-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe49-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fe49-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe49-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe49-154">CommonParameters</span></span>
<span data-ttu-id="1fe49-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe49-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe49-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe49-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe49-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fe49-157">INPUTS</span></span>

## <span data-ttu-id="1fe49-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fe49-158">OUTPUTS</span></span>

### <span data-ttu-id="1fe49-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="1fe49-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1fe49-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fe49-160">NOTES</span></span>

<span data-ttu-id="1fe49-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1fe49-161">ALIASES</span></span>

## <span data-ttu-id="1fe49-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fe49-162">RELATED LINKS</span></span>

