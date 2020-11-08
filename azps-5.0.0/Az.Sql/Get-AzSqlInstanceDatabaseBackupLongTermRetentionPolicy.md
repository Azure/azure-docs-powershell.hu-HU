---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185833"
---
# <span data-ttu-id="167fe-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="167fe-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="167fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="167fe-102">SYNOPSIS</span></span>
<span data-ttu-id="167fe-103">Felügyelt adatbázis hosszú távú adatmegőrzési házirendjét kapja</span><span class="sxs-lookup"><span data-stu-id="167fe-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="167fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="167fe-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="167fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="167fe-105">DESCRIPTION</span></span>
<span data-ttu-id="167fe-106">A **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** parancsmag a felügyelt adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="167fe-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="167fe-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="167fe-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="167fe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="167fe-108">EXAMPLES</span></span>

### <span data-ttu-id="167fe-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="167fe-109">Example 1</span></span>
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

<span data-ttu-id="167fe-110">Az adatbázis hosszú távú adatmegőrzési házirendjének aktuális verzióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="167fe-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="167fe-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="167fe-111">PARAMETERS</span></span>

### <span data-ttu-id="167fe-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="167fe-112">-DatabaseName</span></span>
<span data-ttu-id="167fe-113">A használni kívánt Azure felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="167fe-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="167fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167fe-114">-DefaultProfile</span></span>
<span data-ttu-id="167fe-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="167fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="167fe-116">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="167fe-116">-InstanceName</span></span>
<span data-ttu-id="167fe-117">Az az Azure által felügyelt példány neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="167fe-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="167fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="167fe-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="167fe-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="167fe-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="167fe-120">-Confirm</span></span>
<span data-ttu-id="167fe-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="167fe-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167fe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167fe-122">-WhatIf</span></span>
<span data-ttu-id="167fe-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="167fe-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="167fe-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="167fe-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167fe-125">CommonParameters</span></span>
<span data-ttu-id="167fe-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="167fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167fe-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="167fe-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167fe-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="167fe-128">INPUTS</span></span>

### <span data-ttu-id="167fe-129">System. String</span><span class="sxs-lookup"><span data-stu-id="167fe-129">System.String</span></span>

## <span data-ttu-id="167fe-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="167fe-130">OUTPUTS</span></span>

### <span data-ttu-id="167fe-131">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="167fe-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="167fe-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="167fe-132">NOTES</span></span>

## <span data-ttu-id="167fe-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="167fe-133">RELATED LINKS</span></span>

[<span data-ttu-id="167fe-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="167fe-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="167fe-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="167fe-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="167fe-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="167fe-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="167fe-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="167fe-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)