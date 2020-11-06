---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 65758e08002081fd7781a7601729a64bb69ff31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492157"
---
# <span data-ttu-id="b51ba-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="b51ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b51ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b51ba-103">Egy vagy több adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="b51ba-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b51ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b51ba-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b51ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b51ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b51ba-106">A **Get-AzureRmSqlDatabase** parancsmag egy vagy több Azure SQL-adatbázisból áll az Azure SQL adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="b51ba-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="b51ba-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b51ba-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b51ba-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b51ba-108">EXAMPLES</span></span>

### <span data-ttu-id="b51ba-109">Példa 1: az összes adatbázis lekérése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="b51ba-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="b51ba-110">Ez a parancs a server01 nevű kiszolgálón beolvassa az összes adatbázist.</span><span class="sxs-lookup"><span data-stu-id="b51ba-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="b51ba-111">2. példa: adatbázis beszerzése név alapján a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="b51ba-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="b51ba-112">Ez a parancs a Database02 nevű adatbázist egy Server01 nevű kiszolgálóról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b51ba-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="b51ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b51ba-113">PARAMETERS</span></span>

### <span data-ttu-id="b51ba-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b51ba-114">-DatabaseName</span></span>
<span data-ttu-id="b51ba-115">A beolvasandó adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b51ba-115">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51ba-116">-DefaultProfile</span></span>
<span data-ttu-id="b51ba-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b51ba-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b51ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="b51ba-119">Annak az erőforráscsoport a neve, amelyhez az adatbázis-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b51ba-119">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="b51ba-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b51ba-120">-ServerName</span></span>
<span data-ttu-id="b51ba-121">Annak a kiszolgálónak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b51ba-121">Specifies the name of the server to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b51ba-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b51ba-122">-Confirm</span></span>
<span data-ttu-id="b51ba-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b51ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b51ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b51ba-124">-WhatIf</span></span>
<span data-ttu-id="b51ba-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b51ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b51ba-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b51ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b51ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51ba-127">CommonParameters</span></span>
<span data-ttu-id="b51ba-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b51ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51ba-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b51ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51ba-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51ba-130">INPUTS</span></span>

### <span data-ttu-id="b51ba-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="b51ba-131">None</span></span>
<span data-ttu-id="b51ba-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b51ba-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b51ba-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b51ba-133">OUTPUTS</span></span>

### <span data-ttu-id="b51ba-134">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b51ba-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b51ba-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b51ba-135">NOTES</span></span>

## <span data-ttu-id="b51ba-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b51ba-136">RELATED LINKS</span></span>

[<span data-ttu-id="b51ba-137">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="b51ba-138">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-138">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="b51ba-139">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-139">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="b51ba-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="b51ba-141">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b51ba-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


