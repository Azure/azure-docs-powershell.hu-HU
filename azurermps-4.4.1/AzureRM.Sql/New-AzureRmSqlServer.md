---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673094"
---
# <span data-ttu-id="500db-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="500db-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="500db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="500db-102">SYNOPSIS</span></span>
<span data-ttu-id="500db-103">SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="500db-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="500db-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="500db-105">DESCRIPTION</span></span>
<span data-ttu-id="500db-106">A **New-AzureRmSqlServer** parancsmag egy Azure SQL adatbázis-kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="500db-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="500db-107">Példák</span><span class="sxs-lookup"><span data-stu-id="500db-107">EXAMPLES</span></span>

### <span data-ttu-id="500db-108">Példa 1: új Azure SQL adatbázis-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="500db-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="500db-109">Ez a parancs a 12-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="500db-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="500db-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="500db-110">PARAMETERS</span></span>

### <span data-ttu-id="500db-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="500db-111">-AssignIdentity</span></span>
<span data-ttu-id="500db-112">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="500db-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="500db-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="500db-113">-Location</span></span>
<span data-ttu-id="500db-114">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="500db-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="500db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500db-115">-ResourceGroupName</span></span>
<span data-ttu-id="500db-116">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="500db-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="500db-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="500db-117">-ServerName</span></span>
<span data-ttu-id="500db-118">Az új kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="500db-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="500db-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="500db-119">-ServerVersion</span></span>
<span data-ttu-id="500db-120">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="500db-120">Specifies the version of the new server.</span></span> <span data-ttu-id="500db-121">A paraméter elfogadható értékei a következők: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="500db-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="500db-122">A 12,0 11-es verziójú kiszolgáló létrehozásához adja meg a 2,0-ot.</span><span class="sxs-lookup"><span data-stu-id="500db-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="500db-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="500db-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="500db-124">Az SQL-adatbázis kiszolgálójának rendszergazdai hitelesítő adatait adja meg az új kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="500db-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="500db-125">**PSCredential** objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="500db-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="500db-126">További információért írja be a következőt: `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="500db-126">For more information, type `Get-Help
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

### <span data-ttu-id="500db-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="500db-127">-Tags</span></span>
<span data-ttu-id="500db-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="500db-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="500db-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="500db-129">For example:</span></span>

<span data-ttu-id="500db-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="500db-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="500db-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="500db-131">-Confirm</span></span>
<span data-ttu-id="500db-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="500db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500db-133">-WhatIf</span></span>
<span data-ttu-id="500db-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="500db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500db-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="500db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500db-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500db-136">-DefaultProfile</span></span>
<span data-ttu-id="500db-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="500db-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="500db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500db-138">CommonParameters</span></span>
<span data-ttu-id="500db-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="500db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500db-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500db-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500db-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="500db-141">INPUTS</span></span>

## <span data-ttu-id="500db-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="500db-142">OUTPUTS</span></span>

### <span data-ttu-id="500db-143">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="500db-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="500db-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="500db-144">NOTES</span></span>

## <span data-ttu-id="500db-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="500db-145">RELATED LINKS</span></span>

[<span data-ttu-id="500db-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="500db-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="500db-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="500db-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="500db-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="500db-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="500db-149">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="500db-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="500db-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="500db-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
