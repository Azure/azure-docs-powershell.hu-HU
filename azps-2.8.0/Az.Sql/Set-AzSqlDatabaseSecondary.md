---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 7c500ba5ea2494109a99e7c66e084efefc48d2e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839296"
---
# <span data-ttu-id="a2e2e-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2e2e-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="a2e2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e2e-103">Másodlagos adatbázis átváltása elsődlegesként a feladatátvétel kezdeményezéséhez.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="a2e2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2e2e-104">SYNTAX</span></span>

### <span data-ttu-id="a2e2e-105">NoOptionsSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2e2e-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e2e-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="a2e2e-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e2e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="a2e2e-108">A **set-AzSqlDatabaseSecondary** parancsmag a másodlagos adatbázis elsődleges a feladatátvétel kezdeményezéséhez vált.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="a2e2e-109">Ez a parancsmag általános konfigurációs parancsként van tervezve, de jelenleg csak a feladatátvétel kezdeményezésére korlátozódik.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="a2e2e-110">Adja meg a *AllowDataLoss* paramétert, amellyel áramszünet esetén kezdeményezheti az erő-feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="a2e2e-111">A tervezett műveletek végrehajtásakor, például a helyreállítási gyakorlat során nem kell megadnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="a2e2e-112">Az utóbbi esetben a másodlagos adatbázis szinkronizálva van az elsődleges kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="a2e2e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a2e2e-113">EXAMPLES</span></span>

### <span data-ttu-id="a2e2e-114">1: tervezett feladatátvétel kezdeményezése</span><span class="sxs-lookup"><span data-stu-id="a2e2e-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="a2e2e-115">2: kényszeres feladatátvétel kezdeményezése (potenciális adatvesztéssel)</span><span class="sxs-lookup"><span data-stu-id="a2e2e-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="a2e2e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2e2e-116">PARAMETERS</span></span>

### <span data-ttu-id="a2e2e-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="a2e2e-117">-AllowDataLoss</span></span>
<span data-ttu-id="a2e2e-118">Jelzi, hogy ez a feladatátvételi művelet az adatvesztést teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="a2e2e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2e2e-119">-AsJob</span></span>
<span data-ttu-id="a2e2e-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2e2e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2e2e-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2e2e-121">-DatabaseName</span></span>
<span data-ttu-id="a2e2e-122">A másodlagos Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="a2e2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e2e-123">-DefaultProfile</span></span>
<span data-ttu-id="a2e2e-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2e2e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2e2e-125">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="a2e2e-125">-Failover</span></span>
<span data-ttu-id="a2e2e-126">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="a2e2e-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e2e-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a2e2e-128">Annak az erőforráscsoport-csoportnak a neve, amelyhez a partner Azure SQL-adatbázis van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="a2e2e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e2e-129">-ResourceGroupName</span></span>
<span data-ttu-id="a2e2e-130">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez az Azure SQL-adatbázis másodlagos hozzárendelése van.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="a2e2e-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a2e2e-131">-ServerName</span></span>
<span data-ttu-id="a2e2e-132">Annak az SQL-kiszolgálónak a nevét adja meg, amely az Azure SQL-adatbázis másodlagos példányát tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="a2e2e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2e2e-133">-Confirm</span></span>
<span data-ttu-id="a2e2e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e2e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e2e-135">-WhatIf</span></span>
<span data-ttu-id="a2e2e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e2e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e2e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e2e-138">CommonParameters</span></span>
<span data-ttu-id="a2e2e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2e2e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e2e-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2e2e-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e2e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e2e-141">INPUTS</span></span>

### <span data-ttu-id="a2e2e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e2e-142">System.String</span></span>

## <span data-ttu-id="a2e2e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e2e-143">OUTPUTS</span></span>

### <span data-ttu-id="a2e2e-144">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a2e2e-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="a2e2e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2e2e-145">NOTES</span></span>

## <span data-ttu-id="a2e2e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2e2e-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2e2e-147">Új – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2e2e-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="a2e2e-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2e2e-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="a2e2e-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a2e2e-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
