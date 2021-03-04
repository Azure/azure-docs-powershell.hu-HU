---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 4d4581d78b2e1f90ce334fda77107058f2294f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941137"
---
# <span data-ttu-id="6b7d9-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="6b7d9-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="6b7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7d9-103">Új, rugalmas MySQL-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="6b7d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b7d9-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b7d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b7d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6b7d9-106">Új, rugalmas MySQL-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="6b7d9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b7d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6b7d9-108">1. példa: Új rugalmas MySql-kiszolgáló létrehozása argumentumokkal</span><span class="sxs-lookup"><span data-stu-id="6b7d9-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="6b7d9-109">2. példa: Új, rugalmas MySql-kiszolgáló létrehozása alapértelmezett beállítással</span><span class="sxs-lookup"><span data-stu-id="6b7d9-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="6b7d9-110">Ez a parancsmag létrehozza a MySql rugalmas kiszolgálóját alapértelmezett paraméterértékekkel, és létrehozza a kiszolgálót egy új virtuális hálózaton belül, és egy alhálózatot delegál a kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="6b7d9-111">A hely alapértelmezett értékei a 2. nyugat-amerikai régió, a termékváltozat Standard_B1ms, a termékváltozatréteg sivár, a tárterület mérete pedig 10GiB.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="6b7d9-112">Ha meg szeretné találni a kiszolgáló automatikusan létrehozott jelszavát, a ConvertFrom-SecureString konvertálja a "SecuredPassword" tulajdonságot egyszerű szöveggé.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="6b7d9-113">(Például: $server. SecuredPassword | ConvertFrom-SecureString -AsPtext)</span><span class="sxs-lookup"><span data-stu-id="6b7d9-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="6b7d9-114">3. példa: Új rugalmas MySql-kiszolgáló létrehozása virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="6b7d9-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="6b7d9-115">Ez a parancsmag rugalmas MySql-kiszolgálót hoz létre a felhasználó által megadott vnet-azonosítóval vagy vnet névvel.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="6b7d9-116">Ha a virtuális hálózat nem létezik, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="6b7d9-117">4. példa: Új, rugalmas MySql-kiszolgáló létrehozása virtuális hálózattal és alhálózatnévvel</span><span class="sxs-lookup"><span data-stu-id="6b7d9-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="6b7d9-118">Ez a parancsmag rugalmas MySql-kiszolgálót hoz létre vnet névvel, alhálózatnévvel, vnet-előtaggal és alhálózati előtaggal.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="6b7d9-119">Ha a virtuális hálózat és az alhálózat nem létezik, a parancsmag létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="6b7d9-120">7. példa: Új rugalmas MySql-kiszolgáló létrehozása nyilvános hozzáféréssel az összes IP-hez</span><span class="sxs-lookup"><span data-stu-id="6b7d9-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="6b7d9-121">Ez a parancsmag a MySql rugalmas kiszolgálóját az összes IP-címre megnyitja.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="6b7d9-122">8. példa: Új rugalmas MySql-kiszolgáló létrehozása tűzfallal</span><span class="sxs-lookup"><span data-stu-id="6b7d9-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="6b7d9-123">Ez a parancsmag a MySql rugalmas kiszolgálóját adott IP-címekre nyitja meg.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="6b7d9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b7d9-124">PARAMETERS</span></span>

### <span data-ttu-id="6b7d9-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="6b7d9-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="6b7d9-126">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-126">The password of the administrator.</span></span>
<span data-ttu-id="6b7d9-127">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="6b7d9-128">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="6b7d9-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="6b7d9-129">-AdministratorUserName</span></span>
<span data-ttu-id="6b7d9-130">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-130">Administrator username for the server.</span></span>
<span data-ttu-id="6b7d9-131">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="6b7d9-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b7d9-132">-AsJob</span></span>
<span data-ttu-id="6b7d9-133">Futtassa a parancsot feladatként.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="6b7d9-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="6b7d9-134">-BackupRetentionDay</span></span>
<span data-ttu-id="6b7d9-135">A kiszolgáló biztonsági mentési megőrzési napjai.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-135">Backup retention days for the server.</span></span>
<span data-ttu-id="6b7d9-136">A napszám 7 és 35 között van.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="6b7d9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b7d9-137">-DefaultProfile</span></span>
<span data-ttu-id="6b7d9-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b7d9-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="6b7d9-139">-HighAvailability</span></span>
<span data-ttu-id="6b7d9-140">A magas elérhetőségű funkció engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="6b7d9-141">Az alapértelmezett érték le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-141">Default value is Disabled.</span></span>
<span data-ttu-id="6b7d9-142">Alapértelmezett: Letiltva.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b7d9-143">-Location</span><span class="sxs-lookup"><span data-stu-id="6b7d9-143">-Location</span></span>
<span data-ttu-id="6b7d9-144">Az a hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6b7d9-145">-Name</span><span class="sxs-lookup"><span data-stu-id="6b7d9-145">-Name</span></span>
<span data-ttu-id="6b7d9-146">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-146">The name of the server.</span></span>

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

### <span data-ttu-id="6b7d9-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b7d9-147">-NoWait</span></span>
<span data-ttu-id="6b7d9-148">Futtassa a parancsot aszinkron módon.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6b7d9-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6b7d9-149">-PublicAccess</span></span>
<span data-ttu-id="6b7d9-150">Meghatározza a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-150">Determines the public access.</span></span>
<span data-ttu-id="6b7d9-151">Adjon meg egy vagy több IP-címet az engedélyezett IP-címek listájában.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="6b7d9-152">Az IP-címtartományok között kötőjelnek kell lennie, és nem tartalmazhat szóközöket.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="6b7d9-153">A 0.0.0.0 érték megadása nyilvános hozzáférést biztosít az Azure-ban telepített erőforrásokból a kiszolgáló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="6b7d9-154">Ha nem ad meg IP-címet, az a kiszolgálót nyilvános hozzáférési módban állítja be, de nem hoz létre tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="6b7d9-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b7d9-155">-ResourceGroupName</span></span>
<span data-ttu-id="6b7d9-156">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b7d9-157">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="6b7d9-157">-Sku</span></span>
<span data-ttu-id="6b7d9-158">A termékváltozat neve, általában tier + family + cores (szint + családi + cores) (például Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="6b7d9-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6b7d9-159">-SkuTier</span></span>
<span data-ttu-id="6b7d9-160">A kiszolgáló számítási rétege.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-160">Compute tier of the server.</span></span>
<span data-ttu-id="6b7d9-161">Elfogadott értékek: Sorozatos, GeneralPurpose, Memória optimalizálva.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="6b7d9-162">Alapérték: Törhető.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="6b7d9-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="6b7d9-163">-StorageInMb</span></span>
<span data-ttu-id="6b7d9-164">Kiszolgáló számára engedélyezett maximális tárterület.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="6b7d9-165">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="6b7d9-165">-Subnet</span></span>
<span data-ttu-id="6b7d9-166">Egy meglévő alhálózat neve vagy azonosítója, vagy egy új létrehozni szükséges alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="6b7d9-167">Felhívjuk a figyelmét arra, hogy az alhálózatot delegáljuk a Microsoft.DBforMySQL/flexibleServers szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="6b7d9-168">A delegálás után ez az alhálózat semmilyen más típusú Azure-erőforráshoz nem használható.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="6b7d9-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="6b7d9-169">-SubnetPrefix</span></span>
<span data-ttu-id="6b7d9-170">Az új vnet CIDR formátumban való létrehozásakor használni kívánt alhálózati IP-cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="6b7d9-171">Az alapértelmezett érték 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="6b7d9-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b7d9-172">-SubscriptionId</span></span>
<span data-ttu-id="6b7d9-173">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6b7d9-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b7d9-174">-Tag</span></span>
<span data-ttu-id="6b7d9-175">Alkalmazásspecifikus metaadatok kulcsérték-párok formájában.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6b7d9-176">-Version</span><span class="sxs-lookup"><span data-stu-id="6b7d9-176">-Version</span></span>
<span data-ttu-id="6b7d9-177">Kiszolgálói verzió.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-177">Server version.</span></span>

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

### <span data-ttu-id="6b7d9-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="6b7d9-178">-Vnet</span></span>
<span data-ttu-id="6b7d9-179">Meglévő virtuális hálózat neve vagy azonosítója, vagy egy új létrehozatott hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="6b7d9-180">A névnek 2 és 64 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="6b7d9-181">A névnek betűvel vagy számmal kell kezdődnie, betűvel, számmal vagy aláhúzásjellel kell végződnie, és csak betűket, számokat, aláhúzásokat, pontokat vagy kötőjeleket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="6b7d9-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="6b7d9-182">-VnetPrefix</span></span>
<span data-ttu-id="6b7d9-183">Az ÚJ vnet CIDR formátumban való létrehozásakor használni kívánt IP-cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="6b7d9-184">Az alapértelmezett érték 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="6b7d9-185">-Zone</span><span class="sxs-lookup"><span data-stu-id="6b7d9-185">-Zone</span></span>
<span data-ttu-id="6b7d9-186">Elérhetőségi zóna, amelybe ki kellépítenünk az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-186">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="6b7d9-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b7d9-187">-Confirm</span></span>
<span data-ttu-id="6b7d9-188">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b7d9-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b7d9-189">-WhatIf</span></span>
<span data-ttu-id="6b7d9-190">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b7d9-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b7d9-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7d9-192">CommonParameters</span></span>
<span data-ttu-id="6b7d9-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b7d9-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7d9-194">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b7d9-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7d9-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b7d9-195">INPUTS</span></span>

## <span data-ttu-id="6b7d9-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b7d9-196">OUTPUTS</span></span>

### <span data-ttu-id="6b7d9-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6b7d9-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="6b7d9-198">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b7d9-198">NOTES</span></span>

<span data-ttu-id="6b7d9-199">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6b7d9-199">ALIASES</span></span>

## <span data-ttu-id="6b7d9-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b7d9-200">RELATED LINKS</span></span>

