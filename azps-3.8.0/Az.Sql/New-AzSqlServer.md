---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 7a28e29e6ee517d15c6edcd462c274ef3a7dbced
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847402"
---
# <span data-ttu-id="71571-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="71571-101">New-AzSqlServer</span></span>

## <span data-ttu-id="71571-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71571-102">SYNOPSIS</span></span>
<span data-ttu-id="71571-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="71571-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="71571-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71571-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-PublicNetworkAccess <String>] [-MinimalTlsVersion <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71571-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71571-105">DESCRIPTION</span></span>
<span data-ttu-id="71571-106">A **New-AzSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="71571-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="71571-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71571-107">EXAMPLES</span></span>

### <span data-ttu-id="71571-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="71571-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="71571-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="71571-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="71571-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71571-110">PARAMETERS</span></span>

### <span data-ttu-id="71571-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71571-111">-AsJob</span></span>
<span data-ttu-id="71571-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71571-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71571-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="71571-113">-AssignIdentity</span></span>
<span data-ttu-id="71571-114">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="71571-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="71571-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71571-115">-DefaultProfile</span></span>
<span data-ttu-id="71571-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="71571-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="71571-117">-Location</span></span>
<span data-ttu-id="71571-118">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="71571-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="71571-119">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="71571-119">-PublicNetworkAccess</span></span>
<span data-ttu-id="71571-120">Megadhatja, hogy engedélyezve van-e a hozzáférés, és hogy engedélyezve van-e a nyilvános hálózat elérésének engedélyezése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="71571-120">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="71571-121">Ha le van tiltva, csak a privát hivatkozásokon keresztül elérhető kapcsolatok érhetik el ezt a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="71571-121">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71571-122">-ResourceGroupName</span></span>
<span data-ttu-id="71571-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="71571-123">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71571-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="71571-124">-ServerName</span></span>
<span data-ttu-id="71571-125">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71571-125">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-126">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="71571-126">-ServerVersion</span></span>
<span data-ttu-id="71571-127">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71571-127">Specifies the version of the new server.</span></span> <span data-ttu-id="71571-128">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="71571-128">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="71571-129">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="71571-129">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="71571-130">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="71571-130">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="71571-131">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="71571-131">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="71571-132">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="71571-132">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="71571-133">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="71571-133">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-134">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="71571-134">-MinimalTlsVersion</span></span>
<span data-ttu-id="71571-135">Az SQL Server érvényesítéséhez szükséges minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="71571-135">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="71571-136">-Címkék</span><span class="sxs-lookup"><span data-stu-id="71571-136">-Tags</span></span>
<span data-ttu-id="71571-137">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="71571-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="71571-138">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="71571-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71571-139">-Confirm</span></span>
<span data-ttu-id="71571-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71571-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71571-141">-WhatIf</span></span>
<span data-ttu-id="71571-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71571-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71571-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71571-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71571-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71571-144">CommonParameters</span></span>
<span data-ttu-id="71571-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71571-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71571-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71571-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71571-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71571-147">INPUTS</span></span>

### <span data-ttu-id="71571-148">System. String</span><span class="sxs-lookup"><span data-stu-id="71571-148">System.String</span></span>

## <span data-ttu-id="71571-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71571-149">OUTPUTS</span></span>

### <span data-ttu-id="71571-150">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="71571-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="71571-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71571-151">NOTES</span></span>

## <span data-ttu-id="71571-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71571-152">RELATED LINKS</span></span>

[<span data-ttu-id="71571-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="71571-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="71571-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="71571-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="71571-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="71571-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="71571-156">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71571-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="71571-157">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="71571-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
