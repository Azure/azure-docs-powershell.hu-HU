---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c40f8ad000bca3026860ebc328be57e6931a1546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936698"
---
# <span data-ttu-id="7fd67-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7fd67-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="7fd67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd67-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd67-103">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="7fd67-103">Creates a new server.</span></span>

## <span data-ttu-id="7fd67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fd67-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-Zone <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7fd67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fd67-105">DESCRIPTION</span></span>
<span data-ttu-id="7fd67-106">Létrehoz egy új kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="7fd67-106">Creates a new server.</span></span>

## <span data-ttu-id="7fd67-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fd67-107">EXAMPLES</span></span>

### <span data-ttu-id="7fd67-108">1. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása argumentumokkal</span><span class="sxs-lookup"><span data-stu-id="7fd67-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="7fd67-109">2. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása alapértelmezett beállítással</span><span class="sxs-lookup"><span data-stu-id="7fd67-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="7fd67-110">Ez a parancsmag létrehoz egy rugalmas PostgreSql-kiszolgálót alapértelmezett paraméterértékekkel, és kiépíti a kiszolgálót egy új virtuális hálózaton belül, és egy alhálózatot delegál a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="7fd67-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="7fd67-111">A hely alapértelmezett értékei a 2. nyugat-amerikai régió, a termékváltozat Standard_D2s_v3, a termékváltozatréteg a GeneralPurpose, a tárterület mérete pedig 128GiB.</span><span class="sxs-lookup"><span data-stu-id="7fd67-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="7fd67-112">Ha meg szeretné találni a kiszolgáló automatikusan létrehozott jelszavát, a ConvertFrom-SecureString konvertálja a "SecuredPassword" tulajdonságot egyszerű szöveggé.</span><span class="sxs-lookup"><span data-stu-id="7fd67-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="7fd67-113">(Például: $server. SecuredPassword | ConvertFrom-SecureString -AsPtext)</span><span class="sxs-lookup"><span data-stu-id="7fd67-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="7fd67-114">3. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="7fd67-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7fd67-115">Ez a parancsmag a felhasználó által megadott vnet-azonosítóval vagy vnet-névvel létrehozott postgreSql-kiszolgálót hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7fd67-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="7fd67-116">Ha a virtuális hálózat nem létezik, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="7fd67-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="7fd67-117">4. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása virtuális hálózattal és alhálózatnévvel</span><span class="sxs-lookup"><span data-stu-id="7fd67-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7fd67-118">Ez a parancsmag rugalmas PostgreSql-kiszolgálót hoz létre vnet névvel, alhálózatnévvel, vnet-előtaggal és alhálózati előtaggal.</span><span class="sxs-lookup"><span data-stu-id="7fd67-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="7fd67-119">Ha a virtuális hálózat és az alhálózat nem létezik, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="7fd67-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="7fd67-120">7. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása nyilvános hozzáféréssel az összes IP-hez</span><span class="sxs-lookup"><span data-stu-id="7fd67-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="7fd67-121">Ez a parancsmag létrehoz egy rugalmas PostgreSql-kiszolgálót, amely minden IP-címre meg van nyitva.</span><span class="sxs-lookup"><span data-stu-id="7fd67-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="7fd67-122">8. példa: Új rugalmas PostgreSql-kiszolgáló létrehozása tűzfallal</span><span class="sxs-lookup"><span data-stu-id="7fd67-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="7fd67-123">Ez a parancsmag létrehoz egy rugalmas PostgreSql-kiszolgálót, amely adott IP-címekre nyílik meg.</span><span class="sxs-lookup"><span data-stu-id="7fd67-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="7fd67-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fd67-124">PARAMETERS</span></span>

### <span data-ttu-id="7fd67-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7fd67-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7fd67-126">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="7fd67-126">The password of the administrator.</span></span>
<span data-ttu-id="7fd67-127">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="7fd67-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="7fd67-128">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="7fd67-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd67-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="7fd67-129">-AdministratorUserName</span></span>
<span data-ttu-id="7fd67-130">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="7fd67-130">Administrator username for the server.</span></span>
<span data-ttu-id="7fd67-131">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="7fd67-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="7fd67-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fd67-132">-AsJob</span></span>
<span data-ttu-id="7fd67-133">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="7fd67-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="7fd67-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="7fd67-134">-BackupRetentionDay</span></span>
<span data-ttu-id="7fd67-135">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="7fd67-135">Backup retention days for the server.</span></span>
<span data-ttu-id="7fd67-136">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="7fd67-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="7fd67-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd67-137">-DefaultProfile</span></span>
<span data-ttu-id="7fd67-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fd67-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd67-139">-Location</span><span class="sxs-lookup"><span data-stu-id="7fd67-139">-Location</span></span>
<span data-ttu-id="7fd67-140">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="7fd67-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7fd67-141">-Name</span><span class="sxs-lookup"><span data-stu-id="7fd67-141">-Name</span></span>
<span data-ttu-id="7fd67-142">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7fd67-142">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd67-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7fd67-143">-NoWait</span></span>
<span data-ttu-id="7fd67-144">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="7fd67-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7fd67-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="7fd67-145">-PublicAccess</span></span>
<span data-ttu-id="7fd67-146">Meghatározza a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="7fd67-146">Determines the public access.</span></span>
<span data-ttu-id="7fd67-147">Adjon meg egy vagy több IP-címet az engedélyezett IP-címek listájában.</span><span class="sxs-lookup"><span data-stu-id="7fd67-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="7fd67-148">Az IP-címtartományok között kötőjelnek kell lennie, és nem tartalmazhat szóközöket.</span><span class="sxs-lookup"><span data-stu-id="7fd67-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="7fd67-149">A 0.0.0.0 érték megadása nyilvános hozzáférést biztosít az Azure-ban telepített erőforrásokból a kiszolgáló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7fd67-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="7fd67-150">Ha nem ad meg IP-címet, az a kiszolgálót nyilvános hozzáférési módban állítja be, de nem hoz létre tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="7fd67-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="7fd67-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd67-151">-ResourceGroupName</span></span>
<span data-ttu-id="7fd67-152">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="7fd67-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7fd67-153">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="7fd67-153">-Sku</span></span>
<span data-ttu-id="7fd67-154">A termékváltozat neve, általában tier + family + cores (szint + családi + cores) (például Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="7fd67-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="7fd67-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7fd67-155">-SkuTier</span></span>
<span data-ttu-id="7fd67-156">A kiszolgáló számítási rétege.</span><span class="sxs-lookup"><span data-stu-id="7fd67-156">Compute tier of the server.</span></span>
<span data-ttu-id="7fd67-157">Elfogadott értékek: Sorozatos, GeneralPurpose, Memória optimalizálva.</span><span class="sxs-lookup"><span data-stu-id="7fd67-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="7fd67-158">Alapérték: Törhető.</span><span class="sxs-lookup"><span data-stu-id="7fd67-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="7fd67-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="7fd67-159">-StorageInMb</span></span>
<span data-ttu-id="7fd67-160">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="7fd67-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="7fd67-161">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="7fd67-161">-Subnet</span></span>
<span data-ttu-id="7fd67-162">Egy meglévő alhálózat neve vagy azonosítója, vagy egy új létrehozni szükséges alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="7fd67-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="7fd67-163">Felhívjuk a figyelmét arra, hogy az alhálózatot delegáljuk a Microsoft.DBforPostgreSQL/flexibleServers szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="7fd67-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="7fd67-164">A delegálás után ez az alhálózat semmilyen más típusú Azure-erőforráshoz nem használható.</span><span class="sxs-lookup"><span data-stu-id="7fd67-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="7fd67-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="7fd67-165">-SubnetPrefix</span></span>
<span data-ttu-id="7fd67-166">Az új vnet CIDR formátumban való létrehozásakor használni kívánt alhálózati IP-cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="7fd67-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="7fd67-167">Az alapértelmezett érték 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="7fd67-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="7fd67-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fd67-168">-SubscriptionId</span></span>
<span data-ttu-id="7fd67-169">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="7fd67-169">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7fd67-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="7fd67-170">-Tag</span></span>
<span data-ttu-id="7fd67-171">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="7fd67-171">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7fd67-172">-Version</span><span class="sxs-lookup"><span data-stu-id="7fd67-172">-Version</span></span>
<span data-ttu-id="7fd67-173">Kiszolgálói verzió.</span><span class="sxs-lookup"><span data-stu-id="7fd67-173">Server version.</span></span>

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

### <span data-ttu-id="7fd67-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="7fd67-174">-Vnet</span></span>
<span data-ttu-id="7fd67-175">Meglévő virtuális hálózat neve vagy azonosítója, vagy egy új létrehozatott hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="7fd67-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="7fd67-176">A névnek 2 és 64 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7fd67-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="7fd67-177">A névnek betűvel vagy számmal kell kezdődnie, betűvel, számmal vagy aláhúzásjellel kell végződnie, és csak betűket, számokat, aláhúzásokat, pontokat vagy kötőjeleket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="7fd67-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="7fd67-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="7fd67-178">-VnetPrefix</span></span>
<span data-ttu-id="7fd67-179">Az ÚJ vnet CIDR formátumban való létrehozásakor használni kívánt IP-cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="7fd67-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="7fd67-180">Az alapértelmezett érték 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="7fd67-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="7fd67-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="7fd67-181">-Zone</span></span>
<span data-ttu-id="7fd67-182">Elérhetőségi zóna, amelybe ki kellépítenünk az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7fd67-182">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="7fd67-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fd67-183">-Confirm</span></span>
<span data-ttu-id="7fd67-184">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7fd67-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd67-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd67-185">-WhatIf</span></span>
<span data-ttu-id="7fd67-186">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7fd67-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd67-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fd67-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd67-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd67-188">CommonParameters</span></span>
<span data-ttu-id="7fd67-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd67-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd67-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fd67-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd67-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fd67-191">INPUTS</span></span>

## <span data-ttu-id="7fd67-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fd67-192">OUTPUTS</span></span>

### <span data-ttu-id="7fd67-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="7fd67-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="7fd67-194">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fd67-194">NOTES</span></span>

<span data-ttu-id="7fd67-195">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7fd67-195">ALIASES</span></span>

## <span data-ttu-id="7fd67-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fd67-196">RELATED LINKS</span></span>

