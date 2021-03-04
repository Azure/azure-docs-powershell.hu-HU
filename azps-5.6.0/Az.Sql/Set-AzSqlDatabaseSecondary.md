---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: fc0a6bc7fa87a78fedd0416ea1578b9404168dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926258"
---
# <span data-ttu-id="50509-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50509-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="50509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50509-102">SYNOPSIS</span></span>
<span data-ttu-id="50509-103">A feladatátvétel kezdeményezése érdekében elsődlegesre vált egy másodlagos adatbázist.</span><span class="sxs-lookup"><span data-stu-id="50509-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="50509-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50509-104">SYNTAX</span></span>

### <span data-ttu-id="50509-105">NoOptionsSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50509-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50509-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="50509-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50509-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50509-107">DESCRIPTION</span></span>
<span data-ttu-id="50509-108">A **Set-AzSqlDatabaseSecondary** parancsmag egy másodlagos adatbázist elsődleges adatbázisként vált át a feladatátvétel kezdeményezése érdekében.</span><span class="sxs-lookup"><span data-stu-id="50509-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="50509-109">Ez a parancsmag általános konfigurációs parancsként lett kialakítva, de jelenleg feladatátvétel kezdeményezése.</span><span class="sxs-lookup"><span data-stu-id="50509-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="50509-110">Az *AllowDataLoss* paraméter megadásával kényszerített feladatátvételt kezdeményezhet egy kimaradás során.</span><span class="sxs-lookup"><span data-stu-id="50509-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="50509-111">Nem kell megadnia ezt a paramétert egy tervezett művelet, például helyreállítási gyakorlat végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="50509-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="50509-112">Az utóbbi esetben a rendszer szinkronizálja a másodlagos adatbázist az elsődleges adatbázissal a váltás előtt.</span><span class="sxs-lookup"><span data-stu-id="50509-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="50509-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50509-113">EXAMPLES</span></span>

### <span data-ttu-id="50509-114">1. példa: Tervezett feladatátvétel kezdeményezése</span><span class="sxs-lookup"><span data-stu-id="50509-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="50509-115">2. példa: Kényszerített feladatátvétel kezdeményezése (potenciális adatvesztéssel)</span><span class="sxs-lookup"><span data-stu-id="50509-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="50509-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50509-116">PARAMETERS</span></span>

### <span data-ttu-id="50509-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="50509-117">-AllowDataLoss</span></span>
<span data-ttu-id="50509-118">Azt jelzi, hogy ez a feladatátvételi művelet adatvesztést engedélyez.</span><span class="sxs-lookup"><span data-stu-id="50509-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="50509-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50509-119">-AsJob</span></span>
<span data-ttu-id="50509-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="50509-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50509-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="50509-121">-DatabaseName</span></span>
<span data-ttu-id="50509-122">A másodlagos Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50509-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="50509-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50509-123">-DefaultProfile</span></span>
<span data-ttu-id="50509-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="50509-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50509-125">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="50509-125">-Failover</span></span>
<span data-ttu-id="50509-126">Azt jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="50509-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="50509-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50509-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="50509-128">Annak az erőforráscsoportnak a neve, amelyhez a partner Azure SQL-adatbázist hozzárendelt.</span><span class="sxs-lookup"><span data-stu-id="50509-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="50509-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50509-129">-ResourceGroupName</span></span>
<span data-ttu-id="50509-130">Annak az erőforráscsoportnak a neve, amelyhez az Azure SQL Database Secondary van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="50509-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="50509-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50509-131">-ServerName</span></span>
<span data-ttu-id="50509-132">Annak az SQL Servernek a nevét adja meg, amely az Azure SQL Database Secondary adatbázist tárolja.</span><span class="sxs-lookup"><span data-stu-id="50509-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="50509-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50509-133">-Confirm</span></span>
<span data-ttu-id="50509-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50509-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50509-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50509-135">-WhatIf</span></span>
<span data-ttu-id="50509-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50509-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50509-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50509-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50509-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50509-138">CommonParameters</span></span>
<span data-ttu-id="50509-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50509-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50509-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50509-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50509-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50509-141">INPUTS</span></span>

### <span data-ttu-id="50509-142">System.String</span><span class="sxs-lookup"><span data-stu-id="50509-142">System.String</span></span>

## <span data-ttu-id="50509-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50509-143">OUTPUTS</span></span>

### <span data-ttu-id="50509-144">Microsoft.Azure.Commands.Sql.Replikáció.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="50509-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="50509-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50509-145">NOTES</span></span>

## <span data-ttu-id="50509-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50509-146">RELATED LINKS</span></span>

[<span data-ttu-id="50509-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50509-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="50509-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50509-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="50509-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="50509-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
