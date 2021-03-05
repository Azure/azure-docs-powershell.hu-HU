---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: eb84936310be355ece858884a1e27b7cc954cb51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013350"
---
# <span data-ttu-id="158fa-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="158fa-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="158fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158fa-102">SYNOPSIS</span></span>
<span data-ttu-id="158fa-103">Létrehoz egy szolgáltatópéldányt a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="158fa-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="158fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="158fa-104">SYNTAX</span></span>

### <span data-ttu-id="158fa-105">ByString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="158fa-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="158fa-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="158fa-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="158fa-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="158fa-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="158fa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="158fa-108">DESCRIPTION</span></span>
<span data-ttu-id="158fa-109">Létrehoz egy szolgáltatópéldányt a megadott előfizetéshez, erőforráscsoporthoz, SapMonitor névhez és erőforrásnévhez.</span><span class="sxs-lookup"><span data-stu-id="158fa-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="158fa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="158fa-110">EXAMPLES</span></span>

### <span data-ttu-id="158fa-111">1. példa: SAP-monitor példányának létrehozása karakterlánc alapján a HANA-hoz</span><span class="sxs-lookup"><span data-stu-id="158fa-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-112">Ez a parancs az SAP-monitor karakterláncok szerint létrehozott példányát hozza létre a HANA-nak.</span><span class="sxs-lookup"><span data-stu-id="158fa-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="158fa-113">2. példa: SAP-monitor példányának létrehozása a HANA kulcstára alapján</span><span class="sxs-lookup"><span data-stu-id="158fa-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-114">Ez a parancs az SAP-monitor egy példányát hozza létre a HANA kulcstára alapján.</span><span class="sxs-lookup"><span data-stu-id="158fa-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="158fa-115">3. példa: SAP-monitor példányának létrehozása szótár alapján aRinethhaiHaClusterhez</span><span class="sxs-lookup"><span data-stu-id="158fa-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-116">Ez a parancs létrehozza az SAP-monitor egy példányát a DictionarethhaiHaCluster szótára alapján.</span><span class="sxs-lookup"><span data-stu-id="158fa-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="158fa-117">4. példa: SAP-monitor példányának létrehozása szótár alapján aRinethrinOS számára</span><span class="sxs-lookup"><span data-stu-id="158fa-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-118">Ez a parancs az SAP-monitor egy példányát hozza létre szótár alapján aRinethrinOS számára.</span><span class="sxs-lookup"><span data-stu-id="158fa-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="158fa-119">5. példa: SAP-monitor példányának létrehozása szótár alapján az MsSqlServerhez</span><span class="sxs-lookup"><span data-stu-id="158fa-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-120">Ez a parancs létrehozza az SAP-monitor egy példányát az MsSqlServer szótára alapján.</span><span class="sxs-lookup"><span data-stu-id="158fa-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="158fa-121">6. példa: SAP-monitor példányának létrehozása szótár alapján a SapHana számára</span><span class="sxs-lookup"><span data-stu-id="158fa-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="158fa-122">Ez a parancs létrehozza az SAP-monitor egy példányát a SapHana szótára alapján.</span><span class="sxs-lookup"><span data-stu-id="158fa-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="158fa-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="158fa-123">PARAMETERS</span></span>

### <span data-ttu-id="158fa-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="158fa-124">-AsJob</span></span>
<span data-ttu-id="158fa-125">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="158fa-125">Run the command as a job</span></span>

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

### <span data-ttu-id="158fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158fa-126">-DefaultProfile</span></span>
<span data-ttu-id="158fa-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="158fa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158fa-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="158fa-128">-HanaDatabaseName</span></span>
<span data-ttu-id="158fa-129">A SAP HANA-példány adatbázisneve.</span><span class="sxs-lookup"><span data-stu-id="158fa-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="158fa-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="158fa-131">A SAP HANA-példány adatbázisának jelszava.</span><span class="sxs-lookup"><span data-stu-id="158fa-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="158fa-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="158fa-133">A HANA hitelesítő adatokat tartalmazó kulcstár erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="158fa-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="158fa-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="158fa-135">A HANA hitelesítő adatokat tartalmazó kulcstár titkos azonosítója.</span><span class="sxs-lookup"><span data-stu-id="158fa-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="158fa-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="158fa-137">A SAP HANA-példány adatbázisának SQL-portja.</span><span class="sxs-lookup"><span data-stu-id="158fa-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="158fa-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="158fa-139">A SAP HANA-példány adatbázisának felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="158fa-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="158fa-140">-HanaHostname</span></span>
<span data-ttu-id="158fa-141">A SAP HANA-példány állomásneve.</span><span class="sxs-lookup"><span data-stu-id="158fa-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="158fa-142">-InstanceProperty</span></span>
<span data-ttu-id="158fa-143">A HANA-példány tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="158fa-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="158fa-144">-Metadata</span></span>
<span data-ttu-id="158fa-145">A szolgáltatói példány metaadatait tartalmazó JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="158fa-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="158fa-146">-Name</span><span class="sxs-lookup"><span data-stu-id="158fa-146">-Name</span></span>
<span data-ttu-id="158fa-147">A szolgáltatópéldány neve.</span><span class="sxs-lookup"><span data-stu-id="158fa-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158fa-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="158fa-148">-NoWait</span></span>
<span data-ttu-id="158fa-149">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="158fa-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="158fa-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="158fa-150">-ProviderType</span></span>
<span data-ttu-id="158fa-151">A szolgáltatói példány típusa.</span><span class="sxs-lookup"><span data-stu-id="158fa-151">The type of provider instance.</span></span>
<span data-ttu-id="158fa-152">A támogatott értékek: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="158fa-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="158fa-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="158fa-153">-ResourceGroupName</span></span>
<span data-ttu-id="158fa-154">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="158fa-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="158fa-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="158fa-155">-SapMonitorName</span></span>
<span data-ttu-id="158fa-156">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="158fa-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="158fa-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="158fa-157">-SubscriptionId</span></span>
<span data-ttu-id="158fa-158">Előfizetésazonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="158fa-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="158fa-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="158fa-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="158fa-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="158fa-160">-Confirm</span></span>
<span data-ttu-id="158fa-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="158fa-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158fa-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158fa-162">-WhatIf</span></span>
<span data-ttu-id="158fa-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="158fa-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="158fa-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="158fa-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158fa-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158fa-165">CommonParameters</span></span>
<span data-ttu-id="158fa-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158fa-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158fa-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="158fa-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158fa-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="158fa-168">INPUTS</span></span>

## <span data-ttu-id="158fa-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="158fa-169">OUTPUTS</span></span>

### <span data-ttu-id="158fa-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="158fa-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="158fa-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="158fa-171">NOTES</span></span>

<span data-ttu-id="158fa-172">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="158fa-172">ALIASES</span></span>

## <span data-ttu-id="158fa-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="158fa-173">RELATED LINKS</span></span>

