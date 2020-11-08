---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185182"
---
# <span data-ttu-id="c3c72-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c72-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c3c72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3c72-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c72-103">A **set-AzSqlInstanceDatabaseLongTermRetentionBackup** parancsmag a felügyelt adatbázis hosszú távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3c72-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="c3c72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3c72-104">SYNTAX</span></span>

### <span data-ttu-id="c3c72-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3c72-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c72-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c3c72-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c72-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c3c72-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c72-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c3c72-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3c72-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3c72-109">DESCRIPTION</span></span>
<span data-ttu-id="c3c72-110">A **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** parancsmag a felügyelt adatbázis hosszú távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3c72-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="c3c72-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c3c72-111">EXAMPLES</span></span>

### <span data-ttu-id="c3c72-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3c72-112">Example 1</span></span>
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

<span data-ttu-id="c3c72-113">Az adatbázis hosszú távú adatmegőrzési heti szabályait egy hétre állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3c72-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="c3c72-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3c72-114">Example 2</span></span>
```powershell
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

<span data-ttu-id="c3c72-115">Ez a parancs eltávolítja a hosszú távú adatmegőrzési házirendet az adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="c3c72-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="c3c72-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="c3c72-116">Example 3</span></span>

<span data-ttu-id="c3c72-117">A Set-AzSqlInstanceDatabaseLongTermRetentionBackup parancsmag a felügyelt adatbázis hosszú távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3c72-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="c3c72-118">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c3c72-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="c3c72-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3c72-119">PARAMETERS</span></span>

### <span data-ttu-id="c3c72-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3c72-120">-DatabaseName</span></span>
<span data-ttu-id="c3c72-121">A használni kívánt Azure felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c3c72-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="c3c72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c72-122">-DefaultProfile</span></span>
<span data-ttu-id="c3c72-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3c72-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c72-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="c3c72-124">-InstanceName</span></span>
<span data-ttu-id="c3c72-125">Az az Azure által felügyelt példány neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="c3c72-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="c3c72-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="c3c72-126">-MonthlyRetention</span></span>
<span data-ttu-id="c3c72-127">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="c3c72-127">The Monthly Retention.</span></span>
<span data-ttu-id="c3c72-128">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="c3c72-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c3c72-129">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="c3c72-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c72-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c3c72-130">-RemovePolicy</span></span>
<span data-ttu-id="c3c72-131">Ha meg van határozva, az adatbázis házirendje törlődik.</span><span class="sxs-lookup"><span data-stu-id="c3c72-131">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c72-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c72-132">-ResourceGroupName</span></span>
<span data-ttu-id="c3c72-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3c72-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3c72-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="c3c72-134">-WeeklyRetention</span></span>
<span data-ttu-id="c3c72-135">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="c3c72-135">The Weekly Retention.</span></span>
<span data-ttu-id="c3c72-136">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="c3c72-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c3c72-137">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="c3c72-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c72-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="c3c72-138">-WeekOfYear</span></span>
<span data-ttu-id="c3c72-139">Az év hete, 1 – 52, az éves adatmegőrzésre való mentéshez.</span><span class="sxs-lookup"><span data-stu-id="c3c72-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c72-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="c3c72-140">-YearlyRetention</span></span>
<span data-ttu-id="c3c72-141">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="c3c72-141">The Yearly Retention.</span></span>
<span data-ttu-id="c3c72-142">Ha az ISO 8601 karakterlánc helyett csak egy számot továbbítanak, a napok az egységként jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="c3c72-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c3c72-143">A minimum 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="c3c72-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c72-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3c72-144">-Confirm</span></span>
<span data-ttu-id="c3c72-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3c72-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c72-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c72-146">-WhatIf</span></span>
<span data-ttu-id="c3c72-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3c72-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3c72-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3c72-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c72-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c72-149">CommonParameters</span></span>
<span data-ttu-id="c3c72-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3c72-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c72-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3c72-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c72-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c72-152">INPUTS</span></span>

### <span data-ttu-id="c3c72-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c72-153">System.String</span></span>

### <span data-ttu-id="c3c72-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c3c72-154">System.Int32</span></span>

## <span data-ttu-id="c3c72-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c72-155">OUTPUTS</span></span>

### <span data-ttu-id="c3c72-156">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c3c72-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c3c72-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3c72-157">NOTES</span></span>

## <span data-ttu-id="c3c72-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3c72-158">RELATED LINKS</span></span>

[<span data-ttu-id="c3c72-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3c72-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c3c72-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c3c72-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c3c72-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c3c72-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c3c72-162">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c3c72-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)