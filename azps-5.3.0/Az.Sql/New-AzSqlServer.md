---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467142"
---
# <span data-ttu-id="97f2b-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="97f2b-101">New-AzSqlServer</span></span>

## <span data-ttu-id="97f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="97f2b-103">SQL-adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="97f2b-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="97f2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97f2b-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f2b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="97f2b-106">A **New-AzSqlServer** parancsmag létrehoz egy Azure SQL Database-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="97f2b-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="97f2b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="97f2b-108">1. példa: Új Azure SQL-adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="97f2b-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="97f2b-109">Ez a parancs egy 12-es verziójú Azure SQL Database-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="97f2b-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="97f2b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="97f2b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97f2b-111">-AsJob</span></span>
<span data-ttu-id="97f2b-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="97f2b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97f2b-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="97f2b-113">-AssignIdentity</span></span>
<span data-ttu-id="97f2b-114">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a kiszolgálóhoz olyan kulcskezelő szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="97f2b-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="97f2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f2b-115">-DefaultProfile</span></span>
<span data-ttu-id="97f2b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97f2b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97f2b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="97f2b-117">-Location</span></span>
<span data-ttu-id="97f2b-118">Megadja annak az adatközpontnak a helyét, ahol ez a parancsmag létrehozza a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="97f2b-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="97f2b-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="97f2b-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="97f2b-120">Az Sql Serverhez kényszerítendő minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="97f2b-120">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="97f2b-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="97f2b-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="97f2b-122">Ahhoz, hogy a nyilvános hálózati hozzáférés engedélyezett legyen-e a kiszolgálóhoz, jelölőt kell megadni, illetve letiltani.</span><span class="sxs-lookup"><span data-stu-id="97f2b-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="97f2b-123">Ha le van tiltva, csak a privát hivatkozásokon keresztül létesított kapcsolatok érik el ezt a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="97f2b-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="97f2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="97f2b-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="97f2b-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="97f2b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97f2b-126">-ServerName</span></span>
<span data-ttu-id="97f2b-127">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97f2b-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="97f2b-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="97f2b-128">-ServerVersion</span></span>
<span data-ttu-id="97f2b-129">Az új kiszolgáló verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="97f2b-129">Specifies the version of the new server.</span></span> <span data-ttu-id="97f2b-130">A paraméter elfogadható értékei: 2,0 és 12.0.</span><span class="sxs-lookup"><span data-stu-id="97f2b-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="97f2b-131">Adja meg a 2.0 értéket a 11-es verziójú kiszolgáló létrehozásához, illetve a 12.0 értéket a 12-es verziójú kiszolgáló létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="97f2b-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="97f2b-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="97f2b-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="97f2b-133">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="97f2b-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="97f2b-134">**PSCredential** objektum beszerzéséhez használja a Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="97f2b-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="97f2b-135">További információért írja be a `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="97f2b-135">For more information, type `Get-Help
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

### <span data-ttu-id="97f2b-136">-Címkék</span><span class="sxs-lookup"><span data-stu-id="97f2b-136">-Tags</span></span>
<span data-ttu-id="97f2b-137">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="97f2b-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97f2b-138">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="97f2b-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97f2b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97f2b-139">-Confirm</span></span>
<span data-ttu-id="97f2b-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="97f2b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97f2b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f2b-141">-WhatIf</span></span>
<span data-ttu-id="97f2b-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="97f2b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97f2b-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97f2b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97f2b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f2b-144">CommonParameters</span></span>
<span data-ttu-id="97f2b-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f2b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f2b-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97f2b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f2b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97f2b-147">INPUTS</span></span>

### <span data-ttu-id="97f2b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="97f2b-148">System.String</span></span>

## <span data-ttu-id="97f2b-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97f2b-149">OUTPUTS</span></span>

### <span data-ttu-id="97f2b-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="97f2b-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="97f2b-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97f2b-151">NOTES</span></span>

## <span data-ttu-id="97f2b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97f2b-152">RELATED LINKS</span></span>

[<span data-ttu-id="97f2b-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="97f2b-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="97f2b-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="97f2b-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="97f2b-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="97f2b-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="97f2b-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97f2b-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="97f2b-157">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="97f2b-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
