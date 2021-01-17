---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331217"
---
# <span data-ttu-id="9f3f1-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="9f3f1-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="9f3f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3f1-103">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-103">Creates a new server.</span></span>

## <span data-ttu-id="9f3f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f3f1-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f3f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f3f1-105">DESCRIPTION</span></span>
<span data-ttu-id="9f3f1-106">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-106">Creates a new server.</span></span>

## <span data-ttu-id="9f3f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f3f1-107">EXAMPLES</span></span>

### <span data-ttu-id="9f3f1-108">1. példa: Új PostgreSql-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="9f3f1-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9f3f1-109">Ezek a parancsmagok új PostgreSql-kiszolgálót hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="9f3f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f3f1-110">PARAMETERS</span></span>

### <span data-ttu-id="9f3f1-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="9f3f1-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="9f3f1-112">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9f3f1-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="9f3f1-113">-AdministratorUserName</span></span>
<span data-ttu-id="9f3f1-114">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9f3f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f3f1-115">-AsJob</span></span>
<span data-ttu-id="9f3f1-116">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="9f3f1-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="9f3f1-117">-BackupRetentionDay</span></span>
<span data-ttu-id="9f3f1-118">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-118">Backup retention days for the server.</span></span>
<span data-ttu-id="9f3f1-119">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="9f3f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3f1-120">-DefaultProfile</span></span>
<span data-ttu-id="9f3f1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f3f1-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="9f3f1-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="9f3f1-123">Engedélyezze a georedundáns helymeghatározást, vagy ne engedélyezze a kiszolgáló biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3f1-124">-Location</span><span class="sxs-lookup"><span data-stu-id="9f3f1-124">-Location</span></span>
<span data-ttu-id="9f3f1-125">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="9f3f1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9f3f1-126">-Name</span></span>
<span data-ttu-id="9f3f1-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-127">The name of the server.</span></span>

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

### <span data-ttu-id="9f3f1-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f3f1-128">-NoWait</span></span>
<span data-ttu-id="9f3f1-129">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="9f3f1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f3f1-130">-ResourceGroupName</span></span>
<span data-ttu-id="9f3f1-131">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9f3f1-132">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="9f3f1-132">-Sku</span></span>
<span data-ttu-id="9f3f1-133">A termékváltozat neve, jellemzően tier + family + cores (réteg + család + cores) (például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="9f3f1-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="9f3f1-134">-SslEnforcement</span></span>
<span data-ttu-id="9f3f1-135">Engedélyezze az ssl kényszerítési funkcióját, vagy ne a kiszolgálóhoz való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3f1-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="9f3f1-136">-StorageAutogrow</span></span>
<span data-ttu-id="9f3f1-137">Tárterület automatikus növekedésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3f1-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="9f3f1-138">-StorageInMb</span></span>
<span data-ttu-id="9f3f1-139">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="9f3f1-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f3f1-140">-SubscriptionId</span></span>
<span data-ttu-id="9f3f1-141">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9f3f1-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f3f1-142">-Tag</span></span>
<span data-ttu-id="9f3f1-143">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="9f3f1-144">-Verzió</span><span class="sxs-lookup"><span data-stu-id="9f3f1-144">-Version</span></span>
<span data-ttu-id="9f3f1-145">Kiszolgálóverzió.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3f1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f3f1-146">-Confirm</span></span>
<span data-ttu-id="9f3f1-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f3f1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f3f1-148">-WhatIf</span></span>
<span data-ttu-id="9f3f1-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f3f1-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f3f1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3f1-151">CommonParameters</span></span>
<span data-ttu-id="9f3f1-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f3f1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3f1-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f3f1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3f1-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f3f1-154">INPUTS</span></span>

## <span data-ttu-id="9f3f1-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f3f1-155">OUTPUTS</span></span>

### <span data-ttu-id="9f3f1-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="9f3f1-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9f3f1-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f3f1-157">NOTES</span></span>

<span data-ttu-id="9f3f1-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9f3f1-158">ALIASES</span></span>

## <span data-ttu-id="9f3f1-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f3f1-159">RELATED LINKS</span></span>

