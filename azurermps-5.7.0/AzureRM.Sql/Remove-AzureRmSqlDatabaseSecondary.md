---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501343"
---
# <span data-ttu-id="59d47-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="59d47-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="59d47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59d47-102">SYNOPSIS</span></span>
<span data-ttu-id="59d47-103">Az SQL-adatbázis és a megadott másodlagos adatbázis közötti adatreplikáció megszüntetése</span><span class="sxs-lookup"><span data-stu-id="59d47-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59d47-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d47-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59d47-105">DESCRIPTION</span></span>
<span data-ttu-id="59d47-106">A **Remove-AzureRmSqlDatabaseSecondary** parancsmag a Geo-replikációs hivatkozás megszüntetését kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="59d47-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="59d47-107">Ez a parancsmag az Stop-AzureSqlDatabaseCopy parancsmagot cseréli le.</span><span class="sxs-lookup"><span data-stu-id="59d47-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="59d47-108">A megszakítás előtt nincs replikációs szinkronizálás.</span><span class="sxs-lookup"><span data-stu-id="59d47-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="59d47-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59d47-109">EXAMPLES</span></span>

## <span data-ttu-id="59d47-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59d47-110">PARAMETERS</span></span>

### <span data-ttu-id="59d47-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59d47-111">-DatabaseName</span></span>
<span data-ttu-id="59d47-112">Annak az elsődleges Azure SQL-adatbázisnak a neve, amely a parancsmag által eltávolított replikációs hivatkozással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="59d47-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d47-113">-DefaultProfile</span></span>
<span data-ttu-id="59d47-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59d47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d47-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d47-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="59d47-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59d47-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d47-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="59d47-117">-PartnerServerName</span></span>
<span data-ttu-id="59d47-118">Adja meg a partner SQL-kiszolgálójának nevét.</span><span class="sxs-lookup"><span data-stu-id="59d47-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d47-119">-ResourceGroupName</span></span>
<span data-ttu-id="59d47-120">Az eltávolítandó replikációs hivatkozással társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59d47-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="59d47-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="59d47-121">-ServerName</span></span>
<span data-ttu-id="59d47-122">Annak az SQL-kiszolgálónak a nevét adja meg, amelynek a replikációs hivatkozását el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="59d47-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="59d47-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59d47-123">-Confirm</span></span>
<span data-ttu-id="59d47-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59d47-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d47-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d47-125">-WhatIf</span></span>
<span data-ttu-id="59d47-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59d47-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d47-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59d47-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d47-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d47-128">CommonParameters</span></span>
<span data-ttu-id="59d47-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59d47-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d47-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d47-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d47-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d47-131">INPUTS</span></span>

###  
<span data-ttu-id="59d47-132">Az elsődleges vagy másodlagos adatbázis **adatbázis** -objektumának az adott parancsmaghoz tartozó példányait lehet pipe-ként bekapcsolni.</span><span class="sxs-lookup"><span data-stu-id="59d47-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="59d47-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59d47-133">OUTPUTS</span></span>

###  
<span data-ttu-id="59d47-134">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="59d47-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="59d47-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59d47-135">NOTES</span></span>

## <span data-ttu-id="59d47-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59d47-136">RELATED LINKS</span></span>

[<span data-ttu-id="59d47-137">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="59d47-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="59d47-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="59d47-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="59d47-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59d47-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
