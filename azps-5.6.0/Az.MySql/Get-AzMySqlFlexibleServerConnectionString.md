---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011957"
---
# <span data-ttu-id="dff84-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="dff84-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="dff84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dff84-102">SYNOPSIS</span></span>
<span data-ttu-id="dff84-103">Szerezze be a kapcsolati karakterláncot az ügyfélkapcsolatszolgáltatónak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="dff84-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="dff84-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dff84-104">SYNTAX</span></span>

### <span data-ttu-id="dff84-105">Bejő (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dff84-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dff84-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dff84-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dff84-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dff84-107">DESCRIPTION</span></span>
<span data-ttu-id="dff84-108">Szerezze be a kapcsolati karakterláncot az ügyfélkapcsolatszolgáltatónak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="dff84-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="dff84-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dff84-109">EXAMPLES</span></span>

### <span data-ttu-id="dff84-110">1. példa: Kapcsolati karakterlánc lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="dff84-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="dff84-111">Ez a parancsmag egy ügyfél kapcsolati karakterláncát jeleníti meg kiszolgálónév szerint.</span><span class="sxs-lookup"><span data-stu-id="dff84-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="dff84-112">2. példa: A MySql-kiszolgáló kapcsolati karakterláncának lekérte identitás szerint</span><span class="sxs-lookup"><span data-stu-id="dff84-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="dff84-113">Ez a parancsmag identitás szerint kapja meg a MySql-kiszolgáló kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="dff84-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="dff84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dff84-114">PARAMETERS</span></span>

### <span data-ttu-id="dff84-115">-Client</span><span class="sxs-lookup"><span data-stu-id="dff84-115">-Client</span></span>
<span data-ttu-id="dff84-116">Ügyfélkapcsolat-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="dff84-116">Client connection provider.</span></span>

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

### <span data-ttu-id="dff84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff84-117">-DefaultProfile</span></span>
<span data-ttu-id="dff84-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dff84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dff84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dff84-119">-InputObject</span></span>
<span data-ttu-id="dff84-120">A kapcsolati karakterlánc kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="dff84-120">The server for the connection string.</span></span>
<span data-ttu-id="dff84-121">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="dff84-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dff84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dff84-122">-Name</span></span>
<span data-ttu-id="dff84-123">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dff84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff84-124">-ResourceGroupName</span></span>
<span data-ttu-id="dff84-125">Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="dff84-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dff84-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dff84-126">-SubscriptionId</span></span>
<span data-ttu-id="dff84-127">Az Azure-előfizetést azonosító előfizetésazonosító.</span><span class="sxs-lookup"><span data-stu-id="dff84-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dff84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff84-128">CommonParameters</span></span>
<span data-ttu-id="dff84-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff84-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dff84-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff84-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dff84-131">INPUTS</span></span>

### <span data-ttu-id="dff84-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dff84-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="dff84-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dff84-133">OUTPUTS</span></span>

### <span data-ttu-id="dff84-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dff84-134">System.String</span></span>

## <span data-ttu-id="dff84-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dff84-135">NOTES</span></span>

<span data-ttu-id="dff84-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dff84-136">ALIASES</span></span>

<span data-ttu-id="dff84-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="dff84-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dff84-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dff84-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dff84-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dff84-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dff84-140">INPUTOBJECT: <IMySqlIdentity> A kapcsolati karakterlánc kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="dff84-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="dff84-141">`[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dff84-142">`[DatabaseName <String>]`: Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dff84-143">`[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dff84-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dff84-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dff84-145">`[KeyName <String>]`: A kiszolgálókulcs neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="dff84-146">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dff84-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dff84-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="dff84-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="dff84-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dff84-150">`[ServerName <String>]`: A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dff84-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dff84-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dff84-152">`[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="dff84-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dff84-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dff84-153">RELATED LINKS</span></span>

