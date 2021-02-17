---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1cbc4b8274a619514268e8412f7f9123a5e9e58a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169418"
---
# <span data-ttu-id="81d86-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="81d86-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="81d86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d86-102">SYNOPSIS</span></span>
<span data-ttu-id="81d86-103">Az adatbázis-kiszolgálóval létesít kapcsolat tesztelése</span><span class="sxs-lookup"><span data-stu-id="81d86-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="81d86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81d86-104">SYNTAX</span></span>

### <span data-ttu-id="81d86-105">Teszt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81d86-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81d86-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="81d86-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81d86-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81d86-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81d86-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="81d86-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81d86-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81d86-109">DESCRIPTION</span></span>
<span data-ttu-id="81d86-110">Az adatbázis-kiszolgálóval létesít kapcsolat tesztelése</span><span class="sxs-lookup"><span data-stu-id="81d86-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="81d86-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81d86-111">EXAMPLES</span></span>

### <span data-ttu-id="81d86-112">1. példa: Kapcsolat tesztelése név szerint</span><span class="sxs-lookup"><span data-stu-id="81d86-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="81d86-113">Kapcsolat tesztelése az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="81d86-114">2. példa: Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="81d86-115">Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-115">Test connection by the identity</span></span>

### <span data-ttu-id="81d86-116">3. példa: Lekérdezés tesztelése név szerint</span><span class="sxs-lookup"><span data-stu-id="81d86-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="81d86-117">Lekérdezés tesztelése az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="81d86-118">4. példa: Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="81d86-119">Lekérdezés tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="81d86-119">Test a query by the identity</span></span>

## <span data-ttu-id="81d86-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81d86-120">PARAMETERS</span></span>

### <span data-ttu-id="81d86-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="81d86-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="81d86-122">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="81d86-122">The password of the administrator.</span></span>
<span data-ttu-id="81d86-123">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="81d86-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="81d86-124">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="81d86-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="81d86-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="81d86-125">-AdministratorUserName</span></span>
<span data-ttu-id="81d86-126">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="81d86-126">Administrator username for the server.</span></span>
<span data-ttu-id="81d86-127">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="81d86-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="81d86-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81d86-128">-DatabaseName</span></span>
<span data-ttu-id="81d86-129">A csatlakoztatni megfelelő adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-129">The database name to connect.</span></span>

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

### <span data-ttu-id="81d86-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d86-130">-DefaultProfile</span></span>
<span data-ttu-id="81d86-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81d86-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d86-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d86-132">-InputObject</span></span>
<span data-ttu-id="81d86-133">A csatlakoztatni megfelelő kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="81d86-133">The server to connect.</span></span>
<span data-ttu-id="81d86-134">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="81d86-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d86-135">-Name</span><span class="sxs-lookup"><span data-stu-id="81d86-135">-Name</span></span>
<span data-ttu-id="81d86-136">A csatlakoztatni megfelelő kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d86-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="81d86-137">-QueryText</span></span>
<span data-ttu-id="81d86-138">A tesztelni fog az adatbázis lekérdezése</span><span class="sxs-lookup"><span data-stu-id="81d86-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d86-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d86-139">-ResourceGroupName</span></span>
<span data-ttu-id="81d86-140">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="81d86-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d86-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d86-141">CommonParameters</span></span>
<span data-ttu-id="81d86-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d86-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d86-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81d86-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d86-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81d86-144">INPUTS</span></span>

### <span data-ttu-id="81d86-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="81d86-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="81d86-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81d86-146">OUTPUTS</span></span>

### <span data-ttu-id="81d86-147">System.String</span><span class="sxs-lookup"><span data-stu-id="81d86-147">System.String</span></span>

## <span data-ttu-id="81d86-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81d86-148">NOTES</span></span>

<span data-ttu-id="81d86-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="81d86-149">ALIASES</span></span>

<span data-ttu-id="81d86-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="81d86-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81d86-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="81d86-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81d86-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81d86-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81d86-153">INPUTOBJECT: <IPostgreSqlIdentity> A csatlakoztatni szükséges kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="81d86-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="81d86-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81d86-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81d86-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81d86-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="81d86-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81d86-158">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81d86-159">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="81d86-160">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="81d86-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="81d86-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81d86-162">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81d86-163">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="81d86-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="81d86-164">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="81d86-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81d86-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81d86-165">RELATED LINKS</span></span>

