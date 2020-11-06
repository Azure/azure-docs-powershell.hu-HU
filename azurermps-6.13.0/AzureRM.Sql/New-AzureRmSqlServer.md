---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 208d72607397cb61e098052cd1835f44d4e0e4a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497256"
---
# <span data-ttu-id="c8d20-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c8d20-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="c8d20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8d20-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d20-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c8d20-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8d20-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8d20-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d20-106">A **New-AzureRmSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8d20-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="c8d20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8d20-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d20-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="c8d20-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="c8d20-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c8d20-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="c8d20-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8d20-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d20-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8d20-111">-AsJob</span></span>
<span data-ttu-id="c8d20-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c8d20-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8d20-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c8d20-113">-AssignIdentity</span></span>
<span data-ttu-id="c8d20-114">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="c8d20-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c8d20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d20-115">-DefaultProfile</span></span>
<span data-ttu-id="c8d20-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8d20-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d20-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="c8d20-117">-Location</span></span>
<span data-ttu-id="c8d20-118">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c8d20-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="c8d20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d20-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8d20-120">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="c8d20-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="c8d20-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c8d20-121">-ServerName</span></span>
<span data-ttu-id="c8d20-122">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8d20-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="c8d20-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c8d20-123">-ServerVersion</span></span>
<span data-ttu-id="c8d20-124">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8d20-124">Specifies the version of the new server.</span></span> <span data-ttu-id="c8d20-125">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="c8d20-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="c8d20-126">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="c8d20-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="c8d20-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="c8d20-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="c8d20-128">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="c8d20-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="c8d20-129">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c8d20-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="c8d20-130">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c8d20-130">For more information, type `Get-Help
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

### <span data-ttu-id="c8d20-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="c8d20-131">-Tags</span></span>
<span data-ttu-id="c8d20-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="c8d20-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8d20-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c8d20-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8d20-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8d20-134">-Confirm</span></span>
<span data-ttu-id="c8d20-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8d20-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d20-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d20-136">-WhatIf</span></span>
<span data-ttu-id="c8d20-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8d20-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d20-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8d20-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d20-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d20-139">CommonParameters</span></span>
<span data-ttu-id="c8d20-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8d20-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d20-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d20-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d20-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d20-142">INPUTS</span></span>

### <span data-ttu-id="c8d20-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d20-143">System.String</span></span>

## <span data-ttu-id="c8d20-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d20-144">OUTPUTS</span></span>

### <span data-ttu-id="c8d20-145">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c8d20-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c8d20-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8d20-146">NOTES</span></span>

## <span data-ttu-id="c8d20-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8d20-147">RELATED LINKS</span></span>

[<span data-ttu-id="c8d20-148">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c8d20-148">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="c8d20-149">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c8d20-149">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="c8d20-150">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c8d20-150">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="c8d20-151">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c8d20-151">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c8d20-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c8d20-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
