---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301775"
---
# <span data-ttu-id="4238e-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4238e-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="4238e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4238e-102">SYNOPSIS</span></span>
<span data-ttu-id="4238e-103">Egy adatbázis geo biztonsági mentési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="4238e-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="4238e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4238e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4238e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4238e-105">DESCRIPTION</span></span>
<span data-ttu-id="4238e-106">A **set-AzSqlDatabaseGeoBackupPolicy** parancsmag az adatbázishoz regisztrált térinformatikai biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="4238e-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="4238e-107">Ez egy olyan Azure Backup-erőforrás, amely a biztonságimásolat-tárolási házirend definiálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="4238e-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="4238e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4238e-108">EXAMPLES</span></span>

## <span data-ttu-id="4238e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4238e-109">PARAMETERS</span></span>

### <span data-ttu-id="4238e-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4238e-110">-DatabaseName</span></span>
<span data-ttu-id="4238e-111">Annak az adatbázisnak a neve, amelyhez a parancsmag a Geo biztonsági házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="4238e-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="4238e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4238e-112">-DefaultProfile</span></span>
<span data-ttu-id="4238e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4238e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4238e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4238e-114">-ResourceGroupName</span></span>
<span data-ttu-id="4238e-115">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4238e-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="4238e-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4238e-116">-ServerName</span></span>
<span data-ttu-id="4238e-117">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4238e-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4238e-118">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="4238e-118">-State</span></span>
<span data-ttu-id="4238e-119">A Geo biztonságimásolat-házirend államát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4238e-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="4238e-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4238e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4238e-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4238e-121">Enabled</span></span> 
- <span data-ttu-id="4238e-122">Tiltva</span><span class="sxs-lookup"><span data-stu-id="4238e-122">Disabled</span></span>

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

### <span data-ttu-id="4238e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4238e-123">-Confirm</span></span>
<span data-ttu-id="4238e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4238e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4238e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4238e-125">-WhatIf</span></span>
<span data-ttu-id="4238e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4238e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4238e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4238e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4238e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4238e-128">CommonParameters</span></span>
<span data-ttu-id="4238e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4238e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4238e-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4238e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4238e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4238e-131">INPUTS</span></span>

### <span data-ttu-id="4238e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4238e-132">System.String</span></span>

## <span data-ttu-id="4238e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4238e-133">OUTPUTS</span></span>

### <span data-ttu-id="4238e-134">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4238e-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="4238e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4238e-135">NOTES</span></span>

## <span data-ttu-id="4238e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4238e-136">RELATED LINKS</span></span>

[<span data-ttu-id="4238e-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4238e-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="4238e-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4238e-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

