---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672830"
---
# <span data-ttu-id="09e44-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="09e44-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="09e44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09e44-102">SYNOPSIS</span></span>
<span data-ttu-id="09e44-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="09e44-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09e44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09e44-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09e44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09e44-105">DESCRIPTION</span></span>
<span data-ttu-id="09e44-106">A **New-AzureRmSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="09e44-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="09e44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09e44-107">EXAMPLES</span></span>

### <span data-ttu-id="09e44-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="09e44-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="09e44-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="09e44-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="09e44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09e44-110">PARAMETERS</span></span>

### <span data-ttu-id="09e44-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09e44-111">-AsJob</span></span>
<span data-ttu-id="09e44-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="09e44-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="09e44-113">-AssignIdentity</span></span>
<span data-ttu-id="09e44-114">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="09e44-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e44-115">-DefaultProfile</span></span>
<span data-ttu-id="09e44-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="09e44-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="09e44-117">-Location</span></span>
<span data-ttu-id="09e44-118">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="09e44-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e44-119">-ResourceGroupName</span></span>
<span data-ttu-id="09e44-120">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="09e44-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="09e44-121">-ServerName</span></span>
<span data-ttu-id="09e44-122">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09e44-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="09e44-123">-ServerVersion</span></span>
<span data-ttu-id="09e44-124">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09e44-124">Specifies the version of the new server.</span></span> <span data-ttu-id="09e44-125">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="09e44-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="09e44-126">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="09e44-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="09e44-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="09e44-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="09e44-128">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="09e44-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="09e44-129">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09e44-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="09e44-130">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="09e44-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="09e44-131">-Tags</span></span>
<span data-ttu-id="09e44-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="09e44-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="09e44-133">Példa:</span><span class="sxs-lookup"><span data-stu-id="09e44-133">For example:</span></span>

<span data-ttu-id="09e44-134">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="09e44-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09e44-135">-Confirm</span></span>
<span data-ttu-id="09e44-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09e44-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e44-137">-WhatIf</span></span>
<span data-ttu-id="09e44-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09e44-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e44-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09e44-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e44-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e44-140">CommonParameters</span></span>
<span data-ttu-id="09e44-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09e44-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e44-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e44-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e44-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09e44-143">INPUTS</span></span>

### <span data-ttu-id="09e44-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="09e44-144">None</span></span>
<span data-ttu-id="09e44-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="09e44-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09e44-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09e44-146">OUTPUTS</span></span>

### <span data-ttu-id="09e44-147">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="09e44-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="09e44-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09e44-148">NOTES</span></span>

## <span data-ttu-id="09e44-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09e44-149">RELATED LINKS</span></span>

[<span data-ttu-id="09e44-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="09e44-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="09e44-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="09e44-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="09e44-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="09e44-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="09e44-153">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="09e44-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="09e44-154">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="09e44-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
