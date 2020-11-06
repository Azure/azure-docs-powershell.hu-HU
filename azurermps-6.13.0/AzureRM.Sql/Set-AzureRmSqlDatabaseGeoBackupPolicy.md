---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: c7aa097318f65cd2506ccfcd96e4d9eeeaf9d1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493918"
---
# <span data-ttu-id="af581-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="af581-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="af581-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af581-102">SYNOPSIS</span></span>
<span data-ttu-id="af581-103">Egy adatbázis geo biztonsági mentési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="af581-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af581-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af581-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af581-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af581-105">DESCRIPTION</span></span>
<span data-ttu-id="af581-106">A **set-AzureRmSqlDatabaseGeoBackupPolicy** parancsmag az adatbázishoz regisztrált térinformatikai biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="af581-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="af581-107">Ez egy olyan Azure Backup-erőforrás, amely a biztonságimásolat-tárolási házirend definiálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="af581-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="af581-108">Példák</span><span class="sxs-lookup"><span data-stu-id="af581-108">EXAMPLES</span></span>

## <span data-ttu-id="af581-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af581-109">PARAMETERS</span></span>

### <span data-ttu-id="af581-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af581-110">-DatabaseName</span></span>
<span data-ttu-id="af581-111">Annak az adatbázisnak a neve, amelyhez a parancsmag a Geo biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="af581-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="af581-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af581-112">-DefaultProfile</span></span>
<span data-ttu-id="af581-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af581-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af581-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af581-114">-ResourceGroupName</span></span>
<span data-ttu-id="af581-115">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="af581-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="af581-116">-ServerName</span></span>
<span data-ttu-id="af581-117">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="af581-118">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="af581-118">-State</span></span>
<span data-ttu-id="af581-119">A Geo biztonságimásolat-házirend államát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af581-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="af581-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="af581-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af581-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="af581-121">Enabled</span></span> 
- <span data-ttu-id="af581-122">Tiltva</span><span class="sxs-lookup"><span data-stu-id="af581-122">Disabled</span></span>

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

### <span data-ttu-id="af581-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af581-123">-Confirm</span></span>
<span data-ttu-id="af581-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af581-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af581-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af581-125">-WhatIf</span></span>
<span data-ttu-id="af581-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af581-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af581-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af581-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af581-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af581-128">CommonParameters</span></span>
<span data-ttu-id="af581-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af581-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af581-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af581-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af581-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af581-131">INPUTS</span></span>

### <span data-ttu-id="af581-132">System. String</span><span class="sxs-lookup"><span data-stu-id="af581-132">System.String</span></span>

## <span data-ttu-id="af581-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af581-133">OUTPUTS</span></span>

### <span data-ttu-id="af581-134">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="af581-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="af581-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af581-135">NOTES</span></span>

## <span data-ttu-id="af581-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af581-136">RELATED LINKS</span></span>

[<span data-ttu-id="af581-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="af581-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="af581-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="af581-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

