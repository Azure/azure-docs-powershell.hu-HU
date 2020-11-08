---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014288"
---
# <span data-ttu-id="d3a1f-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a1f-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d3a1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a1f-103">Felügyelt adatbázis hosszú távú adatmegőrzési házirendjét kapja</span><span class="sxs-lookup"><span data-stu-id="d3a1f-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="d3a1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3a1f-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3a1f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a1f-106">A **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** parancsmag a felügyelt adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="d3a1f-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d3a1f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d3a1f-108">EXAMPLES</span></span>

### <span data-ttu-id="d3a1f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3a1f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="d3a1f-110">Az adatbázis hosszú távú adatmegőrzési házirendjének aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="d3a1f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3a1f-111">PARAMETERS</span></span>

### <span data-ttu-id="d3a1f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3a1f-112">-DatabaseName</span></span>
<span data-ttu-id="d3a1f-113">A használni kívánt Azure felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="d3a1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a1f-114">-DefaultProfile</span></span>
<span data-ttu-id="d3a1f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a1f-116">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="d3a1f-116">-InstanceName</span></span>
<span data-ttu-id="d3a1f-117">Az az Azure által felügyelt példány neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="d3a1f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a1f-118">-ResourceGroupName</span></span>
<span data-ttu-id="d3a1f-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3a1f-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3a1f-120">-Confirm</span></span>
<span data-ttu-id="d3a1f-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a1f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a1f-122">-WhatIf</span></span>
<span data-ttu-id="d3a1f-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a1f-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a1f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a1f-125">CommonParameters</span></span>
<span data-ttu-id="d3a1f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3a1f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a1f-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a1f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3a1f-128">INPUTS</span></span>

### <span data-ttu-id="d3a1f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a1f-129">System.String</span></span>

## <span data-ttu-id="d3a1f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3a1f-130">OUTPUTS</span></span>

### <span data-ttu-id="d3a1f-131">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d3a1f-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d3a1f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3a1f-132">NOTES</span></span>

## <span data-ttu-id="d3a1f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3a1f-133">RELATED LINKS</span></span>

[<span data-ttu-id="d3a1f-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3a1f-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d3a1f-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3a1f-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d3a1f-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a1f-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d3a1f-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d3a1f-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)