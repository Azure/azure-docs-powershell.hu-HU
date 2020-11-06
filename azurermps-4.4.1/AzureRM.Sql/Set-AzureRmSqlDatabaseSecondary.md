---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494609"
---
# <span data-ttu-id="ee522-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee522-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ee522-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee522-102">SYNOPSIS</span></span>
<span data-ttu-id="ee522-103">Másodlagos adatbázis átváltása elsődlegesként a feladatátvétel kezdeményezéséhez.</span><span class="sxs-lookup"><span data-stu-id="ee522-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee522-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee522-104">SYNTAX</span></span>

### <span data-ttu-id="ee522-105">NoOptionsSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee522-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee522-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="ee522-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee522-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee522-107">DESCRIPTION</span></span>
<span data-ttu-id="ee522-108">A **set-AzureRmSqlDatabaseSecondary** parancsmag a másodlagos adatbázis elsődleges a feladatátvétel kezdeményezéséhez vált.</span><span class="sxs-lookup"><span data-stu-id="ee522-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="ee522-109">Ez a parancsmag általános konfigurációs parancsként van tervezve, de jelenleg csak a feladatátvétel kezdeményezésére korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="ee522-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="ee522-110">Adja meg a *AllowDataLoss* paramétert, amellyel áramszünet esetén kezdeményezheti az erő-feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="ee522-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="ee522-111">A tervezett műveletek végrehajtásakor, például a helyreállítási gyakorlat során nem kell megadnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="ee522-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="ee522-112">Az utóbbi esetben a másodlagos adatbázis szinkronizálva van az elsődleges kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="ee522-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="ee522-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ee522-113">EXAMPLES</span></span>

## <span data-ttu-id="ee522-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee522-114">PARAMETERS</span></span>

### <span data-ttu-id="ee522-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ee522-115">-AllowDataLoss</span></span>
<span data-ttu-id="ee522-116">Jelzi, hogy ez a feladatátvételi művelet az adatvesztést teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="ee522-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee522-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee522-117">-DatabaseName</span></span>
<span data-ttu-id="ee522-118">A másodlagos Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee522-118">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="ee522-119">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="ee522-119">-Failover</span></span>
<span data-ttu-id="ee522-120">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="ee522-120">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee522-121">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee522-121">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ee522-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez a partner Azure SQL-adatbázis van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ee522-122">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ee522-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee522-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee522-124">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez az Azure SQL-adatbázis másodlagos hozzárendelése van.</span><span class="sxs-lookup"><span data-stu-id="ee522-124">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="ee522-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ee522-125">-ServerName</span></span>
<span data-ttu-id="ee522-126">Annak az SQL-kiszolgálónak a nevét adja meg, amely az Azure SQL-adatbázis másodlagos példányát tárolja.</span><span class="sxs-lookup"><span data-stu-id="ee522-126">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="ee522-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee522-127">-Confirm</span></span>
<span data-ttu-id="ee522-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee522-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee522-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee522-129">-WhatIf</span></span>
<span data-ttu-id="ee522-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee522-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee522-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee522-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee522-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee522-132">-DefaultProfile</span></span>
<span data-ttu-id="ee522-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee522-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee522-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee522-134">CommonParameters</span></span>
<span data-ttu-id="ee522-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee522-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee522-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee522-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee522-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee522-137">INPUTS</span></span>

###  
<span data-ttu-id="ee522-138">A másodlagos adatbázishoz tartozó adatbázis-objektumokat az **adatbázis** -objektum példányaira is áthelyezheti, és az elsődleges adatbázis áttekinthetővé teheti ezt a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee522-138">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="ee522-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee522-139">OUTPUTS</span></span>

###  
<span data-ttu-id="ee522-140">Ez a parancsmag egy **ReplicationLink** ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ee522-140">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="ee522-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee522-141">NOTES</span></span>

## <span data-ttu-id="ee522-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee522-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee522-143">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee522-143">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ee522-144">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee522-144">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ee522-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ee522-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
