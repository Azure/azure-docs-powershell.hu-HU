---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 05b090de647f1c6e6abfb7f2c83e5bd0a4cf616b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501599"
---
# <span data-ttu-id="6f9f2-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="6f9f2-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="6f9f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9f2-103">A Geo-replikációs kapcsolatokat az Azure SQL-adatbázis és egy erőforráscsoport vagy SQL-kiszolgáló között kapja.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f9f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f9f2-104">SYNTAX</span></span>

### <span data-ttu-id="6f9f2-105">ByDatabaseName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f9f2-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9f2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="6f9f2-108">A **Get-AzureRMSqlDatabaseReplicationLink** parancsmag lecseréli a **Get-AzureSqlDatabaseCopy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="6f9f2-109">A megadott Azure SQL-adatbázis és egy erőforráscsoport vagy AzureSQL-kiszolgáló között minden geo-replikációs kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="6f9f2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f9f2-110">EXAMPLES</span></span>

## <span data-ttu-id="6f9f2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f9f2-111">PARAMETERS</span></span>

### <span data-ttu-id="6f9f2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-112">-DatabaseName</span></span>
<span data-ttu-id="6f9f2-113">Annak az SQL-adatbázisnak a neve, amelyből a hivatkozásokat le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="6f9f2-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6f9f2-115">Annak az erőforrás-csoportnak a neve, amelyhez a partner hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-116">-PartnerServerName</span></span>
<span data-ttu-id="6f9f2-117">A partner Azure SQL Server-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="6f9f2-119">Annak az adatbázisnak az Azure-erőforráscsoport nevét adja meg, amelynek a hivatkozásait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="6f9f2-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6f9f2-120">-ServerName</span></span>
<span data-ttu-id="6f9f2-121">Annak az SQL-kiszolgálónak a nevét adja meg, amelybe a hivatkozásokat le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="6f9f2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f9f2-122">-Confirm</span></span>
<span data-ttu-id="6f9f2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9f2-124">-WhatIf</span></span>
<span data-ttu-id="6f9f2-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f9f2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9f2-127">-DefaultProfile</span></span>
<span data-ttu-id="6f9f2-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f9f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9f2-129">CommonParameters</span></span>
<span data-ttu-id="6f9f2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f9f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9f2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9f2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9f2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f9f2-132">INPUTS</span></span>

###  
<span data-ttu-id="6f9f2-133">Ez a parancsmag az elsődleges vagy másodlagos adatbázis **ReplicationLink** vagy **adatbázis** -objektumának példányait fogadja el.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="6f9f2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f9f2-134">OUTPUTS</span></span>

###  
<span data-ttu-id="6f9f2-135">Ez a parancsmag egy **ReplicationLink** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="6f9f2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f9f2-136">NOTES</span></span>

## <span data-ttu-id="6f9f2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f9f2-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f9f2-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6f9f2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
