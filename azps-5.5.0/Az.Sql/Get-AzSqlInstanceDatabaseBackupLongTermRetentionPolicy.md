---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168755"
---
# <span data-ttu-id="d5826-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5826-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d5826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5826-102">SYNOPSIS</span></span>
<span data-ttu-id="d5826-103">Felügyelt adatbázis hosszú távú adatmegőrzési házirendje</span><span class="sxs-lookup"><span data-stu-id="d5826-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="d5826-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5826-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5826-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5826-105">DESCRIPTION</span></span>
<span data-ttu-id="d5826-106">A **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy parancsmag** megkapja a felügyelt adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="d5826-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="d5826-107">A házirend egy Azure biztonságimásolat-erőforrás, amely a biztonságimásolat-tárolási házirend meghatározásához használatos.</span><span class="sxs-lookup"><span data-stu-id="d5826-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d5826-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5826-108">EXAMPLES</span></span>

### <span data-ttu-id="d5826-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="d5826-109">Example 1</span></span>
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

<span data-ttu-id="d5826-110">Az adatbázis hosszú távú adatmegőrzési házirendének aktuális verzióját kapja meg</span><span class="sxs-lookup"><span data-stu-id="d5826-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="d5826-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5826-111">PARAMETERS</span></span>

### <span data-ttu-id="d5826-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5826-112">-DatabaseName</span></span>
<span data-ttu-id="d5826-113">A használni használt Azure Felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d5826-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="d5826-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5826-114">-DefaultProfile</span></span>
<span data-ttu-id="d5826-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5826-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5826-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d5826-116">-InstanceName</span></span>
<span data-ttu-id="d5826-117">Annak az Azure Felügyelt példánynak a neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="d5826-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="d5826-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5826-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5826-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5826-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5826-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5826-120">-Confirm</span></span>
<span data-ttu-id="d5826-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d5826-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5826-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5826-122">-WhatIf</span></span>
<span data-ttu-id="d5826-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d5826-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5826-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5826-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5826-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5826-125">CommonParameters</span></span>
<span data-ttu-id="d5826-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5826-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5826-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5826-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5826-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5826-128">INPUTS</span></span>

### <span data-ttu-id="d5826-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5826-129">System.String</span></span>

## <span data-ttu-id="d5826-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5826-130">OUTPUTS</span></span>

### <span data-ttu-id="d5826-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d5826-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d5826-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5826-132">NOTES</span></span>

## <span data-ttu-id="d5826-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5826-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5826-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d5826-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d5826-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d5826-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d5826-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5826-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d5826-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d5826-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)