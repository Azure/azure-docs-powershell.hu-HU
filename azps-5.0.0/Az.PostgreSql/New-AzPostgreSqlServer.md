---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186366"
---
# <span data-ttu-id="e21a8-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="e21a8-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="e21a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e21a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e21a8-103">Új kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e21a8-103">Creates a new server.</span></span>

## <span data-ttu-id="e21a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e21a8-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e21a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e21a8-105">DESCRIPTION</span></span>
<span data-ttu-id="e21a8-106">Új kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e21a8-106">Creates a new server.</span></span>

## <span data-ttu-id="e21a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e21a8-107">EXAMPLES</span></span>

### <span data-ttu-id="e21a8-108">1. példa: új PostgreSql-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="e21a8-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e21a8-109">Ezekkel a parancsmagokkal új PostgreSql-kiszolgálót hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="e21a8-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="e21a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e21a8-110">PARAMETERS</span></span>

### <span data-ttu-id="e21a8-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e21a8-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="e21a8-112">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="e21a8-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e21a8-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="e21a8-113">-AdministratorUserName</span></span>
<span data-ttu-id="e21a8-114">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="e21a8-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e21a8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e21a8-115">-AsJob</span></span>
<span data-ttu-id="e21a8-116">Futtassa a parancsot munkaként.</span><span class="sxs-lookup"><span data-stu-id="e21a8-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="e21a8-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="e21a8-117">-BackupRetentionDay</span></span>
<span data-ttu-id="e21a8-118">A kiszolgáló biztonságimásolat-adatmegőrzési napjai</span><span class="sxs-lookup"><span data-stu-id="e21a8-118">Backup retention days for the server.</span></span>
<span data-ttu-id="e21a8-119">A napok száma 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="e21a8-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="e21a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21a8-120">-DefaultProfile</span></span>
<span data-ttu-id="e21a8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e21a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21a8-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="e21a8-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="e21a8-123">Engedélyezze a Geo-redundáns vagy nem a kiszolgáló biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="e21a8-123">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="e21a8-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="e21a8-124">-Location</span></span>
<span data-ttu-id="e21a8-125">Az a hely, ahol az erőforrás tartózkodik.</span><span class="sxs-lookup"><span data-stu-id="e21a8-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e21a8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e21a8-126">-Name</span></span>
<span data-ttu-id="e21a8-127">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="e21a8-127">The name of the server.</span></span>

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

### <span data-ttu-id="e21a8-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="e21a8-128">-NoWait</span></span>
<span data-ttu-id="e21a8-129">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="e21a8-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e21a8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21a8-130">-ResourceGroupName</span></span>
<span data-ttu-id="e21a8-131">Az erőforrást tartalmazó erőforráscsoport neve az Azure Resource Manager API-ból vagy a portálról szerzi be ezt az értéket.</span><span class="sxs-lookup"><span data-stu-id="e21a8-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e21a8-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="e21a8-132">-Sku</span></span>
<span data-ttu-id="e21a8-133">A SKU neve, általában a Tier + Family + magok, például B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e21a8-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e21a8-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="e21a8-134">-SslEnforcement</span></span>
<span data-ttu-id="e21a8-135">Engedélyezze az SSL-kényszerítést, vagy ne a csatlakozás a kiszolgálóhoz lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e21a8-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="e21a8-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="e21a8-136">-StorageAutogrow</span></span>
<span data-ttu-id="e21a8-137">A tárterület automatikus bővülésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e21a8-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="e21a8-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="e21a8-138">-StorageInMb</span></span>
<span data-ttu-id="e21a8-139">Maximális tárterület a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e21a8-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="e21a8-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e21a8-140">-SubscriptionId</span></span>
<span data-ttu-id="e21a8-141">Az Azure-előfizetést azonosító előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="e21a8-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e21a8-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="e21a8-142">-Tag</span></span>
<span data-ttu-id="e21a8-143">Alkalmazásspecifikus metaadatok kulcs-érték párok formájában.</span><span class="sxs-lookup"><span data-stu-id="e21a8-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e21a8-144">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e21a8-144">-Version</span></span>
<span data-ttu-id="e21a8-145">Kiszolgáló verziója.</span><span class="sxs-lookup"><span data-stu-id="e21a8-145">Server version.</span></span>

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

### <span data-ttu-id="e21a8-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e21a8-146">-Confirm</span></span>
<span data-ttu-id="e21a8-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e21a8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21a8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21a8-148">-WhatIf</span></span>
<span data-ttu-id="e21a8-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e21a8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21a8-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e21a8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21a8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21a8-151">CommonParameters</span></span>
<span data-ttu-id="e21a8-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e21a8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21a8-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e21a8-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21a8-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e21a8-154">INPUTS</span></span>

## <span data-ttu-id="e21a8-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e21a8-155">OUTPUTS</span></span>

### <span data-ttu-id="e21a8-156">Microsoft. Azure. PowerShell. parancsmagok. PostgreSql. models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="e21a8-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e21a8-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e21a8-157">NOTES</span></span>

<span data-ttu-id="e21a8-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e21a8-158">ALIASES</span></span>

## <span data-ttu-id="e21a8-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e21a8-159">RELATED LINKS</span></span>
