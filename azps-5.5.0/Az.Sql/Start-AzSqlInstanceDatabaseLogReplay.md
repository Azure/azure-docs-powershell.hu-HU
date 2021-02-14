---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7fe59a6ae103da1fa0ff40bfd300fdbf183fea33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163138"
---
# <span data-ttu-id="cfcf0-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cfcf0-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="cfcf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcf0-103">Elindítja a napló visszajátszása szolgáltatást a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="cfcf0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cfcf0-104">SYNTAX</span></span>

### <span data-ttu-id="cfcf0-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cfcf0-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfcf0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cfcf0-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfcf0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cfcf0-107">DESCRIPTION</span></span>
<span data-ttu-id="cfcf0-108">A **Start-AzSqlInstanceDatabaseLogReplay** parancsmag elindítja a naplólejátszási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="cfcf0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cfcf0-109">EXAMPLES</span></span>

### <span data-ttu-id="cfcf0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cfcf0-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="cfcf0-111">Ez a parancs új felügyelt adatbázist hoz létre, és a last_backup.bak visszaállításáig visszaállítja a biztonsági másolatokat a megadott tárolóból.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="cfcf0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cfcf0-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="cfcf0-113">Ez a parancs új felügyelt adatbázist hoz létre, és visszaállítja a biztonsági másolatokat a megadott tárolóból, amíg a Complete-AzSqlInstanceDatabaseLogReplay meg nem hívjuk a legutóbbi szükséges biztonsági mentéssel.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="cfcf0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfcf0-114">PARAMETERS</span></span>

### <span data-ttu-id="cfcf0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfcf0-115">-AsJob</span></span>
<span data-ttu-id="cfcf0-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cfcf0-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="cfcf0-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="cfcf0-118">Az a jelző, amely jelzi, hogy a művelet befejezésekor automatikusan be kell-e fejeződni a visszaállítás.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="cfcf0-119">-Collation</span></span>
<span data-ttu-id="cfcf0-120">A használt példányadatbázis szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcf0-121">-DefaultProfile</span></span>
<span data-ttu-id="cfcf0-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfcf0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfcf0-123">-InputObject</span></span>
<span data-ttu-id="cfcf0-124">A példány-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cfcf0-125">-InstanceName</span></span>
<span data-ttu-id="cfcf0-126">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="cfcf0-127">-LastBackupName</span></span>
<span data-ttu-id="cfcf0-128">Az utolsó visszaállítható biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="cfcf0-129">-Name</span></span>
<span data-ttu-id="cfcf0-130">A példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfcf0-131">-PassThru</span></span>
<span data-ttu-id="cfcf0-132">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-132">Defines Whether return the sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfcf0-133">-ResourceGroupName</span></span>
<span data-ttu-id="cfcf0-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="cfcf0-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="cfcf0-136">A tároló sas tokenje.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="cfcf0-137">-StorageContainerUri</span></span>
<span data-ttu-id="cfcf0-138">A tároló URI-ja.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfcf0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfcf0-139">-Confirm</span></span>
<span data-ttu-id="cfcf0-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfcf0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfcf0-141">-WhatIf</span></span>
<span data-ttu-id="cfcf0-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfcf0-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfcf0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcf0-144">CommonParameters</span></span>
<span data-ttu-id="cfcf0-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcf0-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfcf0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcf0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfcf0-147">INPUTS</span></span>

### <span data-ttu-id="cfcf0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cfcf0-148">System.String</span></span>

### <span data-ttu-id="cfcf0-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cfcf0-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cfcf0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfcf0-150">OUTPUTS</span></span>

### <span data-ttu-id="cfcf0-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cfcf0-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cfcf0-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cfcf0-152">NOTES</span></span>

## <span data-ttu-id="cfcf0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfcf0-153">RELATED LINKS</span></span>
