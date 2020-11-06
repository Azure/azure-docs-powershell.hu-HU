---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494275"
---
# <span data-ttu-id="fd760-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fd760-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="fd760-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd760-102">SYNOPSIS</span></span>
<span data-ttu-id="fd760-103">Másodlagos adatbázis átváltása elsődlegesként a feladatátvétel kezdeményezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fd760-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd760-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd760-104">SYNTAX</span></span>

### <span data-ttu-id="fd760-105">NoOptionsSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd760-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd760-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="fd760-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd760-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd760-107">DESCRIPTION</span></span>
<span data-ttu-id="fd760-108">A **set-AzureRmSqlDatabaseSecondary** parancsmag a másodlagos adatbázis elsődleges a feladatátvétel kezdeményezéséhez vált.</span><span class="sxs-lookup"><span data-stu-id="fd760-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="fd760-109">Ez a parancsmag általános konfigurációs parancsként van tervezve, de jelenleg csak a feladatátvétel kezdeményezésére korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="fd760-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="fd760-110">Adja meg a *AllowDataLoss* paramétert, amellyel áramszünet esetén kezdeményezheti az erő-feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="fd760-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="fd760-111">A tervezett műveletek végrehajtásakor, például a helyreállítási gyakorlat során nem kell megadnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="fd760-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="fd760-112">Az utóbbi esetben a másodlagos adatbázis szinkronizálva van az elsődleges kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="fd760-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="fd760-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fd760-113">EXAMPLES</span></span>

## <span data-ttu-id="fd760-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd760-114">PARAMETERS</span></span>

### <span data-ttu-id="fd760-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="fd760-115">-AllowDataLoss</span></span>
<span data-ttu-id="fd760-116">Jelzi, hogy ez a feladatátvételi művelet az adatvesztést teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="fd760-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd760-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd760-117">-AsJob</span></span>
<span data-ttu-id="fd760-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd760-118">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="fd760-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd760-119">-DatabaseName</span></span>
<span data-ttu-id="fd760-120">A másodlagos Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd760-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="fd760-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd760-121">-DefaultProfile</span></span>
<span data-ttu-id="fd760-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd760-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd760-123">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="fd760-123">-Failover</span></span>
<span data-ttu-id="fd760-124">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="fd760-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd760-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd760-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="fd760-126">Annak az erőforráscsoport-csoportnak a neve, amelyhez a partner Azure SQL-adatbázis van rendelve.</span><span class="sxs-lookup"><span data-stu-id="fd760-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="fd760-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd760-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd760-128">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez az Azure SQL-adatbázis másodlagos hozzárendelése van.</span><span class="sxs-lookup"><span data-stu-id="fd760-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="fd760-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fd760-129">-ServerName</span></span>
<span data-ttu-id="fd760-130">Annak az SQL-kiszolgálónak a nevét adja meg, amely az Azure SQL-adatbázis másodlagos példányát tárolja.</span><span class="sxs-lookup"><span data-stu-id="fd760-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="fd760-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd760-131">-Confirm</span></span>
<span data-ttu-id="fd760-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd760-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd760-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd760-133">-WhatIf</span></span>
<span data-ttu-id="fd760-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd760-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd760-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd760-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd760-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd760-136">CommonParameters</span></span>
<span data-ttu-id="fd760-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd760-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd760-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd760-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd760-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd760-139">INPUTS</span></span>

###  
<span data-ttu-id="fd760-140">A másodlagos adatbázishoz tartozó adatbázis-objektumokat az **adatbázis** -objektum példányaira is áthelyezheti, és az elsődleges adatbázis áttekinthetővé teheti ezt a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd760-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="fd760-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd760-141">OUTPUTS</span></span>

###  
<span data-ttu-id="fd760-142">Ez a parancsmag egy **ReplicationLink** ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fd760-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="fd760-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd760-143">NOTES</span></span>

## <span data-ttu-id="fd760-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd760-144">RELATED LINKS</span></span>

[<span data-ttu-id="fd760-145">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fd760-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="fd760-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fd760-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="fd760-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fd760-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
