---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 56749c265980fc40ee19b60261641f0c98c25da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497243"
---
# <span data-ttu-id="b4046-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4046-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b4046-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4046-102">SYNOPSIS</span></span>
<span data-ttu-id="b4046-103">Másodlagos adatbázis átváltása elsődlegesként a feladatátvétel kezdeményezéséhez.</span><span class="sxs-lookup"><span data-stu-id="b4046-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4046-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4046-104">SYNTAX</span></span>

### <span data-ttu-id="b4046-105">NoOptionsSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4046-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4046-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="b4046-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4046-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4046-107">DESCRIPTION</span></span>
<span data-ttu-id="b4046-108">A **set-AzureRmSqlDatabaseSecondary** parancsmag a másodlagos adatbázis elsődleges a feladatátvétel kezdeményezéséhez vált.</span><span class="sxs-lookup"><span data-stu-id="b4046-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="b4046-109">Ez a parancsmag általános konfigurációs parancsként van tervezve, de jelenleg csak a feladatátvétel kezdeményezésére korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="b4046-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="b4046-110">Adja meg a *AllowDataLoss* paramétert, amellyel áramszünet esetén kezdeményezheti az erő-feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="b4046-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="b4046-111">A tervezett műveletek végrehajtásakor, például a helyreállítási gyakorlat során nem kell megadnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="b4046-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="b4046-112">Az utóbbi esetben a másodlagos adatbázis szinkronizálva van az elsődleges kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="b4046-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="b4046-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b4046-113">EXAMPLES</span></span>

## <span data-ttu-id="b4046-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4046-114">PARAMETERS</span></span>

### <span data-ttu-id="b4046-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b4046-115">-AllowDataLoss</span></span>
<span data-ttu-id="b4046-116">Jelzi, hogy ez a feladatátvételi művelet az adatvesztést teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="b4046-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="b4046-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4046-117">-AsJob</span></span>
<span data-ttu-id="b4046-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4046-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4046-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4046-119">-DatabaseName</span></span>
<span data-ttu-id="b4046-120">A másodlagos Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4046-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b4046-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4046-121">-DefaultProfile</span></span>
<span data-ttu-id="b4046-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b4046-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4046-123">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="b4046-123">-Failover</span></span>
<span data-ttu-id="b4046-124">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="b4046-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="b4046-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4046-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b4046-126">Annak az erőforráscsoport-csoportnak a neve, amelyhez a partner Azure SQL-adatbázis van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b4046-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b4046-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4046-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4046-128">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez az Azure SQL-adatbázis másodlagos hozzárendelése van.</span><span class="sxs-lookup"><span data-stu-id="b4046-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="b4046-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b4046-129">-ServerName</span></span>
<span data-ttu-id="b4046-130">Annak az SQL-kiszolgálónak a nevét adja meg, amely az Azure SQL-adatbázis másodlagos példányát tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4046-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b4046-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4046-131">-Confirm</span></span>
<span data-ttu-id="b4046-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4046-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4046-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4046-133">-WhatIf</span></span>
<span data-ttu-id="b4046-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4046-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4046-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4046-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4046-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4046-136">CommonParameters</span></span>
<span data-ttu-id="b4046-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4046-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4046-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4046-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4046-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4046-139">INPUTS</span></span>

### <span data-ttu-id="b4046-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b4046-140">System.String</span></span>

## <span data-ttu-id="b4046-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4046-141">OUTPUTS</span></span>

### <span data-ttu-id="b4046-142">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b4046-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b4046-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4046-143">NOTES</span></span>

## <span data-ttu-id="b4046-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4046-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4046-145">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4046-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b4046-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4046-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b4046-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b4046-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
