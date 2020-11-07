---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839353"
---
# <span data-ttu-id="183b3-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="183b3-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="183b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="183b3-102">SYNOPSIS</span></span>
<span data-ttu-id="183b3-103">Egy adatbázis geo biztonsági mentési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="183b3-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="183b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="183b3-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="183b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="183b3-105">DESCRIPTION</span></span>
<span data-ttu-id="183b3-106">A **set-AzSqlDatabaseGeoBackupPolicy** parancsmag az adatbázishoz regisztrált térinformatikai biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="183b3-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="183b3-107">Ez egy olyan Azure Backup-erőforrás, amely a biztonságimásolat-tárolási házirend definiálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="183b3-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="183b3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="183b3-108">EXAMPLES</span></span>

## <span data-ttu-id="183b3-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="183b3-109">PARAMETERS</span></span>

### <span data-ttu-id="183b3-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="183b3-110">-DatabaseName</span></span>
<span data-ttu-id="183b3-111">Annak az adatbázisnak a neve, amelyhez a parancsmag a Geo biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="183b3-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="183b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183b3-112">-DefaultProfile</span></span>
<span data-ttu-id="183b3-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="183b3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="183b3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183b3-114">-ResourceGroupName</span></span>
<span data-ttu-id="183b3-115">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="183b3-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="183b3-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="183b3-116">-ServerName</span></span>
<span data-ttu-id="183b3-117">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="183b3-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="183b3-118">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="183b3-118">-State</span></span>
<span data-ttu-id="183b3-119">A Geo biztonságimásolat-házirend államát adja meg.</span><span class="sxs-lookup"><span data-stu-id="183b3-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="183b3-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="183b3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="183b3-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="183b3-121">Enabled</span></span> 
- <span data-ttu-id="183b3-122">Tiltva</span><span class="sxs-lookup"><span data-stu-id="183b3-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183b3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="183b3-123">-Confirm</span></span>
<span data-ttu-id="183b3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="183b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="183b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="183b3-125">-WhatIf</span></span>
<span data-ttu-id="183b3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="183b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="183b3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="183b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="183b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183b3-128">CommonParameters</span></span>
<span data-ttu-id="183b3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="183b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183b3-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="183b3-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183b3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="183b3-131">INPUTS</span></span>

### <span data-ttu-id="183b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="183b3-132">System.String</span></span>

## <span data-ttu-id="183b3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="183b3-133">OUTPUTS</span></span>

### <span data-ttu-id="183b3-134">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="183b3-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="183b3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="183b3-135">NOTES</span></span>

## <span data-ttu-id="183b3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="183b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="183b3-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="183b3-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="183b3-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="183b3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

