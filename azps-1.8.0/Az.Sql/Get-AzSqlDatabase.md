---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 78fabb521342de2bd5f9b7646df25c54905d50c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669052"
---
# <span data-ttu-id="5d556-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="5d556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d556-102">SYNOPSIS</span></span>
<span data-ttu-id="5d556-103">Egy vagy több adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="5d556-103">Gets one or more databases.</span></span>

## <span data-ttu-id="5d556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d556-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d556-105">DESCRIPTION</span></span>
<span data-ttu-id="5d556-106">A **Get-AzSqlDatabase** parancsmag egy vagy több Azure SQL-adatbázisból áll az Azure SQL adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="5d556-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="5d556-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="5d556-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5d556-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5d556-108">EXAMPLES</span></span>

### <span data-ttu-id="5d556-109">Példa 1: az összes adatbázis lekérése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="5d556-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5d556-110">Ez a parancs a server01 nevű kiszolgálón beolvassa az összes adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5d556-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="5d556-111">2. példa: adatbázis beszerzése név alapján a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="5d556-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5d556-112">Ez a parancs a Database02 nevű adatbázist egy Server01 nevű kiszolgálóról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5d556-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="5d556-113">3. példa: az összes adatbázis beolvasása a kiszolgálón szűréssel</span><span class="sxs-lookup"><span data-stu-id="5d556-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="5d556-114">Ez a parancs a server01 nevű kiszolgálón az "adatbázis" kezdetű adatbázisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5d556-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="5d556-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d556-115">PARAMETERS</span></span>

### <span data-ttu-id="5d556-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d556-116">-DatabaseName</span></span>
<span data-ttu-id="5d556-117">A beolvasandó adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d556-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5d556-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d556-118">-DefaultProfile</span></span>
<span data-ttu-id="5d556-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d556-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d556-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d556-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d556-121">Annak az erőforráscsoport a neve, amelyhez az adatbázis-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5d556-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="5d556-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5d556-122">-ServerName</span></span>
<span data-ttu-id="5d556-123">Annak a kiszolgálónak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5d556-123">Specifies the name of the server to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d556-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d556-124">-Confirm</span></span>
<span data-ttu-id="5d556-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d556-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d556-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d556-126">-WhatIf</span></span>
<span data-ttu-id="5d556-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d556-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d556-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d556-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d556-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d556-129">CommonParameters</span></span>
<span data-ttu-id="5d556-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d556-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d556-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d556-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d556-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d556-132">INPUTS</span></span>

### <span data-ttu-id="5d556-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5d556-133">System.String</span></span>

## <span data-ttu-id="5d556-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d556-134">OUTPUTS</span></span>

### <span data-ttu-id="5d556-135">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5d556-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5d556-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d556-136">NOTES</span></span>

## <span data-ttu-id="5d556-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d556-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d556-138">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5d556-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5d556-140">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5d556-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5d556-142">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d556-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


