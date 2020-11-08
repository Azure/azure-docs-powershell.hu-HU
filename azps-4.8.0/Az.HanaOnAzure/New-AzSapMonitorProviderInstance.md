---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024765"
---
# <span data-ttu-id="e045e-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="e045e-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="e045e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e045e-102">SYNOPSIS</span></span>
<span data-ttu-id="e045e-103">Létrehoz egy szolgáltatói példányt a megadott előfizetéshez, az erőforrás csoporthoz, a SapMonitor és az erőforrás nevéhez.</span><span class="sxs-lookup"><span data-stu-id="e045e-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="e045e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e045e-104">SYNTAX</span></span>

### <span data-ttu-id="e045e-105">ByString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e045e-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e045e-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="e045e-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e045e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e045e-107">DESCRIPTION</span></span>
<span data-ttu-id="e045e-108">Létrehoz egy szolgáltatói példányt a megadott előfizetéshez, az erőforrás csoporthoz, a SapMonitor és az erőforrás nevéhez.</span><span class="sxs-lookup"><span data-stu-id="e045e-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="e045e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e045e-109">EXAMPLES</span></span>

### <span data-ttu-id="e045e-110">1. példa: az SAP-monitorok példányának létrehozása a HANA karakterláncmal</span><span class="sxs-lookup"><span data-stu-id="e045e-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="e045e-111">Ez a parancs az SAP-monitor egy példányát a HANA karakterláncban hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e045e-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="e045e-112">2. példa: az SAP-monitor példányának létrehozása a HANA-alapú kulcs boltozatával</span><span class="sxs-lookup"><span data-stu-id="e045e-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="e045e-113">Ez a parancs az SAP-monitor egy példányát a HANA for HANA (fő pince) segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e045e-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="e045e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e045e-114">PARAMETERS</span></span>

### <span data-ttu-id="e045e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e045e-115">-AsJob</span></span>
<span data-ttu-id="e045e-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e045e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e045e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e045e-117">-DefaultProfile</span></span>
<span data-ttu-id="e045e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e045e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e045e-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e045e-119">-HanaDatabaseName</span></span>
<span data-ttu-id="e045e-120">Az SAP HANA-példány adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="e045e-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e045e-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="e045e-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="e045e-122">A SAP HANA-példány adatbázisának jelszava.</span><span class="sxs-lookup"><span data-stu-id="e045e-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="e045e-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="e045e-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="e045e-124">A HANA-hitelesítő adatokat tartalmazó kulcsfájl erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e045e-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="e045e-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="e045e-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="e045e-126">A titkos azonosító a HANA-hitelesítő adatokat tartalmazó fő Vault-titokhoz.</span><span class="sxs-lookup"><span data-stu-id="e045e-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="e045e-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="e045e-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="e045e-128">Az SAP HANA-példány adatbázisának SQL-portja.</span><span class="sxs-lookup"><span data-stu-id="e045e-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e045e-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="e045e-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="e045e-130">A SAP HANA-példány adatbázisának a felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="e045e-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e045e-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="e045e-131">-HanaHostname</span></span>
<span data-ttu-id="e045e-132">A SAP HANA-példány neve.</span><span class="sxs-lookup"><span data-stu-id="e045e-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="e045e-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e045e-133">-Metadata</span></span>
<span data-ttu-id="e045e-134">A szolgáltató példány metaadatait tartalmazó JSON karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="e045e-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="e045e-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e045e-135">-Name</span></span>
<span data-ttu-id="e045e-136">A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="e045e-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="e045e-137">-Várva</span><span class="sxs-lookup"><span data-stu-id="e045e-137">-NoWait</span></span>
<span data-ttu-id="e045e-138">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e045e-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e045e-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="e045e-139">-ProviderType</span></span>
<span data-ttu-id="e045e-140">A szolgáltató példány típusa.</span><span class="sxs-lookup"><span data-stu-id="e045e-140">The type of provider instance.</span></span>
<span data-ttu-id="e045e-141">A támogatott értékek a következők: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="e045e-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="e045e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e045e-142">-ResourceGroupName</span></span>
<span data-ttu-id="e045e-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e045e-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="e045e-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="e045e-144">-SapMonitorName</span></span>
<span data-ttu-id="e045e-145">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e045e-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="e045e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e045e-146">-SubscriptionId</span></span>
<span data-ttu-id="e045e-147">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e045e-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e045e-148">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e045e-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e045e-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e045e-149">-Confirm</span></span>
<span data-ttu-id="e045e-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e045e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e045e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e045e-151">-WhatIf</span></span>
<span data-ttu-id="e045e-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e045e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e045e-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e045e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e045e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e045e-154">CommonParameters</span></span>
<span data-ttu-id="e045e-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e045e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e045e-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e045e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e045e-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e045e-157">INPUTS</span></span>

## <span data-ttu-id="e045e-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e045e-158">OUTPUTS</span></span>

### <span data-ttu-id="e045e-159">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. modellek. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="e045e-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="e045e-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e045e-160">NOTES</span></span>

<span data-ttu-id="e045e-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e045e-161">ALIASES</span></span>

## <span data-ttu-id="e045e-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e045e-162">RELATED LINKS</span></span>

