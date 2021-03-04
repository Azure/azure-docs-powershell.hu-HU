---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: 5616eb79575154e2cbd5128f10eabc1913c9d506
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927034"
---
# <span data-ttu-id="c375b-101">Test-AzMySqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="c375b-101">Test-AzMySqlFlexibleServerConnect</span></span>

## <span data-ttu-id="c375b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c375b-102">SYNOPSIS</span></span>
<span data-ttu-id="c375b-103">Az adatbázis-kiszolgálóval létesít kapcsolat tesztelése</span><span class="sxs-lookup"><span data-stu-id="c375b-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="c375b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c375b-104">SYNTAX</span></span>

### <span data-ttu-id="c375b-105">Teszt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c375b-105">Test (Default)</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c375b-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="c375b-106">TestAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c375b-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c375b-107">TestViaIdentity</span></span>
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c375b-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="c375b-108">TestViaIdentityAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c375b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c375b-109">DESCRIPTION</span></span>
<span data-ttu-id="c375b-110">Az adatbázis-kiszolgálóval létesít kapcsolat tesztelése</span><span class="sxs-lookup"><span data-stu-id="c375b-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="c375b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c375b-111">EXAMPLES</span></span>

### <span data-ttu-id="c375b-112">1. példa: Kapcsolat tesztelése név szerint</span><span class="sxs-lookup"><span data-stu-id="c375b-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="c375b-113">Kapcsolat tesztelése az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="c375b-114">2. példa: Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="c375b-115">Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-115">Test connection by the identity</span></span>

### <span data-ttu-id="c375b-116">3. példa: Lekérdezés tesztelése név szerint</span><span class="sxs-lookup"><span data-stu-id="c375b-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="c375b-117">Lekérdezés tesztelése az erőforráscsoport és a kiszolgáló neve alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="c375b-118">4. példa: Kapcsolat tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="c375b-119">Lekérdezés tesztelése identitás alapján</span><span class="sxs-lookup"><span data-stu-id="c375b-119">Test a query by the identity</span></span>

## <span data-ttu-id="c375b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c375b-120">PARAMETERS</span></span>

### <span data-ttu-id="c375b-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c375b-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c375b-122">A rendszergazda jelszava.</span><span class="sxs-lookup"><span data-stu-id="c375b-122">The password of the administrator.</span></span>
<span data-ttu-id="c375b-123">Minimum 8 karakter és legfeljebb 128 karakter.</span><span class="sxs-lookup"><span data-stu-id="c375b-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="c375b-124">A jelszónak a következő három kategóriából kell karaktereket tartalmaznia: angol nagybetűk, angol kisbetűk, számok és nem alfanumerikus karakterek.</span><span class="sxs-lookup"><span data-stu-id="c375b-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="c375b-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="c375b-125">-AdministratorUserName</span></span>
<span data-ttu-id="c375b-126">A kiszolgáló rendszergazdai felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="c375b-126">Administrator username for the server.</span></span>
<span data-ttu-id="c375b-127">A beállítás után a beállítás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="c375b-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="c375b-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c375b-128">-DatabaseName</span></span>
<span data-ttu-id="c375b-129">A csatlakoztatni megfelelő adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-129">The database name to connect.</span></span>

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

### <span data-ttu-id="c375b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c375b-130">-DefaultProfile</span></span>
<span data-ttu-id="c375b-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c375b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c375b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c375b-132">-InputObject</span></span>
<span data-ttu-id="c375b-133">A csatlakoztatni megfelelő kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="c375b-133">The server to connect.</span></span>
<span data-ttu-id="c375b-134">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="c375b-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c375b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c375b-135">-Name</span></span>
<span data-ttu-id="c375b-136">A csatlakoztatni megfelelő kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-136">The name of the server to connect.</span></span>

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

### <span data-ttu-id="c375b-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="c375b-137">-QueryText</span></span>
<span data-ttu-id="c375b-138">A tesztelni fog az adatbázis lekérdezése</span><span class="sxs-lookup"><span data-stu-id="c375b-138">The query for the database to test</span></span>

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

### <span data-ttu-id="c375b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c375b-139">-ResourceGroupName</span></span>
<span data-ttu-id="c375b-140">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="c375b-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c375b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c375b-141">CommonParameters</span></span>
<span data-ttu-id="c375b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c375b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c375b-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c375b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c375b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c375b-144">INPUTS</span></span>

### <span data-ttu-id="c375b-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c375b-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c375b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c375b-146">OUTPUTS</span></span>

### <span data-ttu-id="c375b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c375b-147">System.String</span></span>

## <span data-ttu-id="c375b-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c375b-148">NOTES</span></span>

<span data-ttu-id="c375b-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c375b-149">ALIASES</span></span>

<span data-ttu-id="c375b-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c375b-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c375b-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c375b-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c375b-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c375b-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c375b-153">INPUTOBJECT: <IMySqlIdentity> A csatlakoztatni szükséges kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="c375b-153">INPUTOBJECT <IMySqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="c375b-154">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c375b-155">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c375b-156">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c375b-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c375b-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c375b-158">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c375b-159">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c375b-160">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c375b-161">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="c375b-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="c375b-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c375b-163">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c375b-164">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c375b-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c375b-165">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c375b-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c375b-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c375b-166">RELATED LINKS</span></span>

