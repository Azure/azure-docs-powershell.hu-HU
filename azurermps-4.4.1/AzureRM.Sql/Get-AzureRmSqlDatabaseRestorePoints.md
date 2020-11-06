---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: 002b248195840cb7453757e92f9269e7a61d9fda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499128"
---
# <span data-ttu-id="06443-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="06443-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="06443-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06443-102">SYNOPSIS</span></span>
<span data-ttu-id="06443-103">Lekérdezi az SQL-adattárház visszaállítási pontjait.</span><span class="sxs-lookup"><span data-stu-id="06443-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06443-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06443-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06443-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06443-105">DESCRIPTION</span></span>
<span data-ttu-id="06443-106">A **Get-AzureRmSqlDatabaseRestorePoints** parancsmag kikeresi azokat a különálló visszaállítási pontokat, amelyeket egy Azure SQL-adattárházból lehet visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="06443-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="06443-107">Azure SQL-adatbázis esetén a visszaállítási ablak folytonos.</span><span class="sxs-lookup"><span data-stu-id="06443-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="06443-108">Ez azt jelenti, hogy az adatbázis biztonsági adatmegőrzési időszakában bármely időpontban használható visszaállítási pontként.</span><span class="sxs-lookup"><span data-stu-id="06443-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="06443-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="06443-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="06443-110">Példák</span><span class="sxs-lookup"><span data-stu-id="06443-110">EXAMPLES</span></span>

### <span data-ttu-id="06443-111">Példa 1: az összes visszaállítási pont beolvasása</span><span class="sxs-lookup"><span data-stu-id="06443-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
```

<span data-ttu-id="06443-112">Ez a parancs a Database01 nevű Azure SQL-adatbázis minden elérhető visszaállítási pontját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="06443-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="06443-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06443-113">PARAMETERS</span></span>

### <span data-ttu-id="06443-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06443-114">-DatabaseName</span></span>
<span data-ttu-id="06443-115">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06443-115">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06443-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06443-116">-ResourceGroupName</span></span>
<span data-ttu-id="06443-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="06443-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="06443-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="06443-118">-ServerName</span></span>
<span data-ttu-id="06443-119">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06443-119">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="06443-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06443-120">-Confirm</span></span>
<span data-ttu-id="06443-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06443-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06443-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06443-122">-WhatIf</span></span>
<span data-ttu-id="06443-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06443-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06443-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06443-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06443-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06443-125">-DefaultProfile</span></span>
<span data-ttu-id="06443-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06443-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06443-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06443-127">CommonParameters</span></span>
<span data-ttu-id="06443-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06443-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06443-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06443-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06443-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06443-130">INPUTS</span></span>

## <span data-ttu-id="06443-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06443-131">OUTPUTS</span></span>

## <span data-ttu-id="06443-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06443-132">NOTES</span></span>

## <span data-ttu-id="06443-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06443-133">RELATED LINKS</span></span>

