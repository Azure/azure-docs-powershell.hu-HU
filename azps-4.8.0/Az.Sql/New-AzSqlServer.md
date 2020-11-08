---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024351"
---
# <span data-ttu-id="734f5-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="734f5-101">New-AzSqlServer</span></span>

## <span data-ttu-id="734f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="734f5-102">SYNOPSIS</span></span>
<span data-ttu-id="734f5-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="734f5-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="734f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="734f5-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="734f5-105">DESCRIPTION</span></span>
<span data-ttu-id="734f5-106">A **New-AzSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="734f5-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="734f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="734f5-107">EXAMPLES</span></span>

### <span data-ttu-id="734f5-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="734f5-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="734f5-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="734f5-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="734f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="734f5-110">PARAMETERS</span></span>

### <span data-ttu-id="734f5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="734f5-111">-AsJob</span></span>
<span data-ttu-id="734f5-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="734f5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="734f5-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="734f5-113">-AssignIdentity</span></span>
<span data-ttu-id="734f5-114">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="734f5-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="734f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734f5-115">-DefaultProfile</span></span>
<span data-ttu-id="734f5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="734f5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="734f5-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="734f5-117">-Location</span></span>
<span data-ttu-id="734f5-118">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="734f5-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="734f5-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="734f5-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="734f5-120">Az SQL Server érvényesítéséhez szükséges minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="734f5-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734f5-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="734f5-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="734f5-122">Megadhatja, hogy engedélyezve van-e a hozzáférés, és hogy engedélyezve van-e a nyilvános hálózat elérésének engedélyezése a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="734f5-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="734f5-123">Ha le van tiltva, csak a privát hivatkozásokon keresztül elérhető kapcsolatok érhetik el ezt a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="734f5-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="734f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="734f5-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="734f5-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="734f5-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="734f5-126">-ServerName</span></span>
<span data-ttu-id="734f5-127">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="734f5-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="734f5-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="734f5-128">-ServerVersion</span></span>
<span data-ttu-id="734f5-129">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="734f5-129">Specifies the version of the new server.</span></span> <span data-ttu-id="734f5-130">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="734f5-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="734f5-131">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="734f5-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="734f5-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="734f5-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="734f5-133">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="734f5-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="734f5-134">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="734f5-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="734f5-135">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="734f5-135">For more information, type `Get-Help
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

### <span data-ttu-id="734f5-136">-Címkék</span><span class="sxs-lookup"><span data-stu-id="734f5-136">-Tags</span></span>
<span data-ttu-id="734f5-137">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="734f5-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="734f5-138">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="734f5-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="734f5-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="734f5-139">-Confirm</span></span>
<span data-ttu-id="734f5-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="734f5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734f5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734f5-141">-WhatIf</span></span>
<span data-ttu-id="734f5-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="734f5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734f5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="734f5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734f5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734f5-144">CommonParameters</span></span>
<span data-ttu-id="734f5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="734f5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734f5-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="734f5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734f5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="734f5-147">INPUTS</span></span>

### <span data-ttu-id="734f5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="734f5-148">System.String</span></span>

## <span data-ttu-id="734f5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="734f5-149">OUTPUTS</span></span>

### <span data-ttu-id="734f5-150">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="734f5-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="734f5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="734f5-151">NOTES</span></span>

## <span data-ttu-id="734f5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="734f5-152">RELATED LINKS</span></span>

[<span data-ttu-id="734f5-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="734f5-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="734f5-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="734f5-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="734f5-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="734f5-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="734f5-156">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="734f5-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="734f5-157">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="734f5-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
