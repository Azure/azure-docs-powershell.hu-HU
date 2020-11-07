---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846590"
---
# <span data-ttu-id="7d6c5-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d6c5-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="7d6c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6c5-103">A **set-AzSqlInstanceDatabaseLongTermRetentionBackup** parancsmag a felügyelt adatbázis hosszú távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="7d6c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d6c5-104">SYNTAX</span></span>

### <span data-ttu-id="7d6c5-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d6c5-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6c5-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7d6c5-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6c5-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7d6c5-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6c5-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7d6c5-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d6c5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d6c5-109">DESCRIPTION</span></span>
<span data-ttu-id="7d6c5-110">A **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** parancsmag a felügyelt adatbázis hosszú távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="7d6c5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d6c5-111">EXAMPLES</span></span>

### <span data-ttu-id="7d6c5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d6c5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="7d6c5-113">Az adatbázis hosszú távú adatmegőrzési heti szabályait egy hétre állítja be.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="7d6c5-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="7d6c5-114">Example 2</span></span>
```
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```


<span data-ttu-id="7d6c5-115">Ez a parancs eltávolítja a hosszú távú adatmegőrzési házirendet az adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="7d6c5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d6c5-116">PARAMETERS</span></span>

### <span data-ttu-id="7d6c5-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d6c5-117">-DatabaseName</span></span>
<span data-ttu-id="7d6c5-118">A használni kívánt Azure felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-118">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="7d6c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6c5-119">-DefaultProfile</span></span>
<span data-ttu-id="7d6c5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d6c5-121">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="7d6c5-121">-InstanceName</span></span>
<span data-ttu-id="7d6c5-122">Az az Azure által felügyelt példány neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-122">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="7d6c5-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="7d6c5-123">-MonthlyRetention</span></span>
<span data-ttu-id="7d6c5-124">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-124">The Monthly Retention.</span></span>
<span data-ttu-id="7d6c5-125">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7d6c5-126">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c5-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7d6c5-127">-RemovePolicy</span></span>
<span data-ttu-id="7d6c5-128">Ha meg van határozva, az adatbázis házirendje törlődik.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="7d6c5-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d6c5-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="7d6c5-131">-WeeklyRetention</span></span>
<span data-ttu-id="7d6c5-132">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-132">The Weekly Retention.</span></span>
<span data-ttu-id="7d6c5-133">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7d6c5-134">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c5-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="7d6c5-135">-WeekOfYear</span></span>
<span data-ttu-id="7d6c5-136">Az év hete, 1 – 52, az éves adatmegőrzésre való mentéshez.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c5-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="7d6c5-137">-YearlyRetention</span></span>
<span data-ttu-id="7d6c5-138">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-138">The Yearly Retention.</span></span>
<span data-ttu-id="7d6c5-139">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7d6c5-140">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c5-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d6c5-141">-Confirm</span></span>
<span data-ttu-id="7d6c5-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6c5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6c5-143">-WhatIf</span></span>
<span data-ttu-id="7d6c5-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6c5-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6c5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6c5-146">CommonParameters</span></span>
<span data-ttu-id="7d6c5-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d6c5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6c5-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d6c5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6c5-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d6c5-149">INPUTS</span></span>

### <span data-ttu-id="7d6c5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7d6c5-150">System.String</span></span>

### <span data-ttu-id="7d6c5-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7d6c5-151">System.Int32</span></span>

## <span data-ttu-id="7d6c5-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d6c5-152">OUTPUTS</span></span>

### <span data-ttu-id="7d6c5-153">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7d6c5-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="7d6c5-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d6c5-154">NOTES</span></span>

## <span data-ttu-id="7d6c5-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d6c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="7d6c5-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d6c5-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7d6c5-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7d6c5-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7d6c5-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7d6c5-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7d6c5-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7d6c5-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)