---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 37e8896389931f6909d783cbb07a694ed6186fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207119"
---
# <span data-ttu-id="82e05-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="82e05-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="82e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e05-102">SYNOPSIS</span></span>
<span data-ttu-id="82e05-103">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="82e05-103">Creates a new server.</span></span>

## <span data-ttu-id="82e05-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82e05-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82e05-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82e05-105">DESCRIPTION</span></span>
<span data-ttu-id="82e05-106">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="82e05-106">Creates a new server.</span></span>

## <span data-ttu-id="82e05-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82e05-107">EXAMPLES</span></span>

### <span data-ttu-id="82e05-108">1. példa: Új MySql-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="82e05-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="82e05-109">Ezek a parancsmagok új MySql-kiszolgálót hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="82e05-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="82e05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82e05-110">PARAMETERS</span></span>

### <span data-ttu-id="82e05-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="82e05-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="82e05-112">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="82e05-112">The password of the administrator.</span></span>
<span data-ttu-id="82e05-113">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="82e05-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="82e05-114">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="82e05-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="82e05-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="82e05-115">-AdministratorUserName</span></span>
<span data-ttu-id="82e05-116">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="82e05-116">Administrator username for the server.</span></span>
<span data-ttu-id="82e05-117">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="82e05-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="82e05-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82e05-118">-AsJob</span></span>
<span data-ttu-id="82e05-119">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="82e05-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="82e05-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="82e05-120">-BackupRetentionDay</span></span>
<span data-ttu-id="82e05-121">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="82e05-121">Backup retention days for the server.</span></span>
<span data-ttu-id="82e05-122">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="82e05-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="82e05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e05-123">-DefaultProfile</span></span>
<span data-ttu-id="82e05-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82e05-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e05-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="82e05-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="82e05-126">Engedélyezze a georedundáns vagy a nem kiszolgálói biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="82e05-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="82e05-127">-Location</span><span class="sxs-lookup"><span data-stu-id="82e05-127">-Location</span></span>
<span data-ttu-id="82e05-128">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="82e05-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="82e05-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="82e05-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="82e05-130">Állítsa be a minimális TLS-verziót a kiszolgálói kapcsolatokhoz, ha engedélyezve van az SSL.</span><span class="sxs-lookup"><span data-stu-id="82e05-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="82e05-131">A alapértelmezett érték a TLSEnforcementDisabled.accepted érték: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="82e05-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e05-132">-Name</span><span class="sxs-lookup"><span data-stu-id="82e05-132">-Name</span></span>
<span data-ttu-id="82e05-133">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="82e05-133">The name of the server.</span></span>

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

### <span data-ttu-id="82e05-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82e05-134">-NoWait</span></span>
<span data-ttu-id="82e05-135">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="82e05-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="82e05-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e05-136">-ResourceGroupName</span></span>
<span data-ttu-id="82e05-137">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="82e05-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="82e05-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="82e05-138">-Sku</span></span>
<span data-ttu-id="82e05-139">A termékváltozat neve, általában tier + family + cores (szint + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="82e05-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="82e05-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="82e05-140">-SslEnforcement</span></span>
<span data-ttu-id="82e05-141">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="82e05-141">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="82e05-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="82e05-142">-StorageAutogrow</span></span>
<span data-ttu-id="82e05-143">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="82e05-143">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="82e05-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="82e05-144">-StorageInMb</span></span>
<span data-ttu-id="82e05-145">A kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="82e05-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="82e05-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82e05-146">-SubscriptionId</span></span>
<span data-ttu-id="82e05-147">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="82e05-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="82e05-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="82e05-148">-Tag</span></span>
<span data-ttu-id="82e05-149">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="82e05-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="82e05-150">-Version</span><span class="sxs-lookup"><span data-stu-id="82e05-150">-Version</span></span>
<span data-ttu-id="82e05-151">Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="82e05-151">Server version.</span></span>

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

### <span data-ttu-id="82e05-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82e05-152">-Confirm</span></span>
<span data-ttu-id="82e05-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82e05-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82e05-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82e05-154">-WhatIf</span></span>
<span data-ttu-id="82e05-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82e05-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82e05-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82e05-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82e05-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e05-157">CommonParameters</span></span>
<span data-ttu-id="82e05-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e05-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e05-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82e05-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e05-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82e05-160">INPUTS</span></span>

## <span data-ttu-id="82e05-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82e05-161">OUTPUTS</span></span>

### <span data-ttu-id="82e05-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="82e05-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="82e05-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82e05-163">NOTES</span></span>

<span data-ttu-id="82e05-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="82e05-164">ALIASES</span></span>

## <span data-ttu-id="82e05-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82e05-165">RELATED LINKS</span></span>

