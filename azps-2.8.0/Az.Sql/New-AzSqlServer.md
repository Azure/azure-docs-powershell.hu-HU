---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839142"
---
# <span data-ttu-id="1f58a-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f58a-101">New-AzSqlServer</span></span>

## <span data-ttu-id="1f58a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f58a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f58a-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f58a-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="1f58a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f58a-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f58a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f58a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f58a-106">A **New-AzSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f58a-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="1f58a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f58a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f58a-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="1f58a-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="1f58a-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f58a-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="1f58a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f58a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f58a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f58a-111">-AsJob</span></span>
<span data-ttu-id="1f58a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1f58a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f58a-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1f58a-113">-AssignIdentity</span></span>
<span data-ttu-id="1f58a-114">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="1f58a-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1f58a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f58a-115">-DefaultProfile</span></span>
<span data-ttu-id="1f58a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f58a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f58a-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1f58a-117">-Location</span></span>
<span data-ttu-id="1f58a-118">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1f58a-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="1f58a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f58a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f58a-120">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1f58a-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="1f58a-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1f58a-121">-ServerName</span></span>
<span data-ttu-id="1f58a-122">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f58a-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="1f58a-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1f58a-123">-ServerVersion</span></span>
<span data-ttu-id="1f58a-124">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f58a-124">Specifies the version of the new server.</span></span> <span data-ttu-id="1f58a-125">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="1f58a-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="1f58a-126">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="1f58a-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="1f58a-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="1f58a-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="1f58a-128">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="1f58a-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="1f58a-129">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1f58a-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="1f58a-130">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1f58a-130">For more information, type `Get-Help
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

### <span data-ttu-id="1f58a-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="1f58a-131">-Tags</span></span>
<span data-ttu-id="1f58a-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1f58a-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f58a-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1f58a-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f58a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f58a-134">-Confirm</span></span>
<span data-ttu-id="1f58a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f58a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f58a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f58a-136">-WhatIf</span></span>
<span data-ttu-id="1f58a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f58a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f58a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f58a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f58a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f58a-139">CommonParameters</span></span>
<span data-ttu-id="1f58a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f58a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f58a-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f58a-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f58a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f58a-142">INPUTS</span></span>

### <span data-ttu-id="1f58a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1f58a-143">System.String</span></span>

## <span data-ttu-id="1f58a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f58a-144">OUTPUTS</span></span>

### <span data-ttu-id="1f58a-145">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1f58a-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1f58a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f58a-146">NOTES</span></span>

## <span data-ttu-id="1f58a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f58a-147">RELATED LINKS</span></span>

[<span data-ttu-id="1f58a-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f58a-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="1f58a-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f58a-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="1f58a-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f58a-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="1f58a-151">Új – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1f58a-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="1f58a-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1f58a-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
