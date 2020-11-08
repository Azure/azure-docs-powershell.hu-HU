---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024376"
---
# <span data-ttu-id="72361-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="72361-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="72361-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72361-102">SYNOPSIS</span></span>
<span data-ttu-id="72361-103">Az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="72361-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="72361-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72361-104">SYNTAX</span></span>

### <span data-ttu-id="72361-105">ByLocation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72361-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72361-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="72361-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72361-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72361-107">DESCRIPTION</span></span>
<span data-ttu-id="72361-108">A **Get-AzSqlServerServiceObjective** parancsmag elérhetővé válik az Azure SQL adatbázis-kiszolgálók elérhető szolgáltatási céljainak.</span><span class="sxs-lookup"><span data-stu-id="72361-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="72361-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72361-109">EXAMPLES</span></span>

### <span data-ttu-id="72361-110">Példa 1: szolgáltatási célok beszerzése</span><span class="sxs-lookup"><span data-stu-id="72361-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="72361-111">Ez a parancs beolvassa a Server01 nevű kiszolgáló szolgáltatási céljait.</span><span class="sxs-lookup"><span data-stu-id="72361-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="72361-112">2. példa: a szolgáltatási célkitűzések beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="72361-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="72361-113">Ez a parancs a "rendszer" kezdetű Server01 nevű kiszolgáló szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72361-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="72361-114">3. példa: szolgáltatási célok elérése helyhez</span><span class="sxs-lookup"><span data-stu-id="72361-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="72361-115">Ez a parancs a megadott Azure-régióhoz tartozó szolgáltatási célkitűzéseket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72361-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="72361-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72361-116">PARAMETERS</span></span>

### <span data-ttu-id="72361-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72361-117">-DefaultProfile</span></span>
<span data-ttu-id="72361-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72361-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72361-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="72361-119">-Location</span></span>
<span data-ttu-id="72361-120">Annak a helynek a neve, amelybe be szeretné szerezni a szolgáltatási célokat.</span><span class="sxs-lookup"><span data-stu-id="72361-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72361-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72361-121">-ResourceGroupName</span></span>
<span data-ttu-id="72361-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72361-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="72361-123">Ez a parancsmag az erőforráshoz rendelt SQL-adatbázis-kiszolgáló szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="72361-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72361-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="72361-124">-ServerName</span></span>
<span data-ttu-id="72361-125">Egy SQL-adatbázis SQL Server-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72361-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72361-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="72361-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="72361-127">Itt adhatja meg az Azure SQL-adatbázis-kiszolgáló szolgáltatási céljainak a nevét.</span><span class="sxs-lookup"><span data-stu-id="72361-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="72361-128">A paraméter elfogadható értékei a következők: Basic, S0, S1, S2, P1, P2 és P3.</span><span class="sxs-lookup"><span data-stu-id="72361-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72361-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72361-129">-Confirm</span></span>
<span data-ttu-id="72361-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72361-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72361-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72361-131">-WhatIf</span></span>
<span data-ttu-id="72361-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72361-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72361-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72361-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72361-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72361-134">CommonParameters</span></span>
<span data-ttu-id="72361-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72361-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72361-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="72361-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72361-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72361-137">INPUTS</span></span>

### <span data-ttu-id="72361-138">System. String</span><span class="sxs-lookup"><span data-stu-id="72361-138">System.String</span></span>

## <span data-ttu-id="72361-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72361-139">OUTPUTS</span></span>

### <span data-ttu-id="72361-140">Microsoft. Azure. Command. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="72361-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="72361-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72361-141">NOTES</span></span>

## <span data-ttu-id="72361-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72361-142">RELATED LINKS</span></span>

[<span data-ttu-id="72361-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="72361-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


