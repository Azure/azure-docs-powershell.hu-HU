---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346482"
---
# <span data-ttu-id="35f1d-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35f1d-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="35f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="35f1d-103">A **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** parancsmag beállítja a felügyelt adatbázis hosszú távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="35f1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35f1d-104">SYNTAX</span></span>

### <span data-ttu-id="35f1d-105">WeeklyRetentionRequired (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35f1d-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f1d-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="35f1d-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f1d-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="35f1d-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f1d-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="35f1d-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35f1d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35f1d-109">DESCRIPTION</span></span>
<span data-ttu-id="35f1d-110">A **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy parancsmag** hosszú távú adatmegőrzési házirendet állít be ehhez a felügyelt adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="35f1d-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="35f1d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35f1d-111">EXAMPLES</span></span>

### <span data-ttu-id="35f1d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="35f1d-112">Example 1</span></span>
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

<span data-ttu-id="35f1d-113">Az adatbázis hosszú távú heti adatmegőrzési házirendje egy hétre van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="35f1d-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="35f1d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="35f1d-114">Example 2</span></span>
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

<span data-ttu-id="35f1d-115">Ez a parancs eltávolítja a hosszú távú adatmegőrzési házirendet az adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="35f1d-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="35f1d-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="35f1d-116">Example 3</span></span>

<span data-ttu-id="35f1d-117">A Set-AzSqlInstanceDatabaseLongTermRetentionBackup parancsmag beállítja a felügyelt adatbázis hosszú távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="35f1d-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="35f1d-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="35f1d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f1d-119">PARAMETERS</span></span>

### <span data-ttu-id="35f1d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35f1d-120">-DatabaseName</span></span>
<span data-ttu-id="35f1d-121">A használni használt Azure Felügyelt adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="35f1d-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="35f1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f1d-122">-DefaultProfile</span></span>
<span data-ttu-id="35f1d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35f1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f1d-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="35f1d-124">-InstanceName</span></span>
<span data-ttu-id="35f1d-125">Annak az Azure Felügyelt példánynak a neve, amelyhez az adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="35f1d-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="35f1d-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="35f1d-126">-MonthlyRetention</span></span>
<span data-ttu-id="35f1d-127">A havi adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="35f1d-127">The Monthly Retention.</span></span>
<span data-ttu-id="35f1d-128">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="35f1d-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="35f1d-129">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="35f1d-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="35f1d-130">-RemovePolicy</span></span>
<span data-ttu-id="35f1d-131">Ha meg van biztosítanak egy házirendet az adatbázishoz, a rendszer törli a házirendet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="35f1d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f1d-132">-ResourceGroupName</span></span>
<span data-ttu-id="35f1d-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35f1d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="35f1d-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="35f1d-134">-WeeklyRetention</span></span>
<span data-ttu-id="35f1d-135">A heti adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="35f1d-135">The Weekly Retention.</span></span>
<span data-ttu-id="35f1d-136">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="35f1d-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="35f1d-137">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="35f1d-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="35f1d-138">-WeekOfYear</span></span>
<span data-ttu-id="35f1d-139">Az év hetét (1–52) az éves adatmegőrzéshez menteni.</span><span class="sxs-lookup"><span data-stu-id="35f1d-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="35f1d-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="35f1d-140">-YearlyRetention</span></span>
<span data-ttu-id="35f1d-141">Az éves adatmegőrzés.</span><span class="sxs-lookup"><span data-stu-id="35f1d-141">The Yearly Retention.</span></span>
<span data-ttu-id="35f1d-142">Ha iso 8601-es karakterlánc helyett csak egy számot ad át, a napok száma lesz az egység.</span><span class="sxs-lookup"><span data-stu-id="35f1d-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="35f1d-143">Legalább 7 nap és legfeljebb 10 év lehet.</span><span class="sxs-lookup"><span data-stu-id="35f1d-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="35f1d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35f1d-144">-Confirm</span></span>
<span data-ttu-id="35f1d-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35f1d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f1d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f1d-146">-WhatIf</span></span>
<span data-ttu-id="35f1d-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35f1d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f1d-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35f1d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f1d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f1d-149">CommonParameters</span></span>
<span data-ttu-id="35f1d-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f1d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f1d-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35f1d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f1d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35f1d-152">INPUTS</span></span>

### <span data-ttu-id="35f1d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="35f1d-153">System.String</span></span>

### <span data-ttu-id="35f1d-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="35f1d-154">System.Int32</span></span>

## <span data-ttu-id="35f1d-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35f1d-155">OUTPUTS</span></span>

### <span data-ttu-id="35f1d-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="35f1d-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="35f1d-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35f1d-157">NOTES</span></span>

## <span data-ttu-id="35f1d-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35f1d-158">RELATED LINKS</span></span>

[<span data-ttu-id="35f1d-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35f1d-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="35f1d-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="35f1d-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="35f1d-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="35f1d-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="35f1d-162">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="35f1d-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)