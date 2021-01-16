---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332033"
---
# <span data-ttu-id="d990c-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d990c-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="d990c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d990c-102">SYNOPSIS</span></span>
<span data-ttu-id="d990c-103">Elindítja a napló visszajátszása szolgáltatást a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="d990c-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="d990c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d990c-104">SYNTAX</span></span>

### <span data-ttu-id="d990c-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d990c-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d990c-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d990c-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d990c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d990c-107">DESCRIPTION</span></span>
<span data-ttu-id="d990c-108">A **Start-AzSqlInstanceDatabaseLogReplay** parancsmag elindítja a naplólejátszási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d990c-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="d990c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d990c-109">EXAMPLES</span></span>

### <span data-ttu-id="d990c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d990c-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="d990c-111">Ez a parancs új felügyelt adatbázist hoz létre, és a last_backup.bak visszaállításáig visszaállítja a biztonsági másolatokat a megadott tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d990c-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="d990c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d990c-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="d990c-113">Ez a parancs új felügyelt adatbázist hoz létre, és visszaállítja a biztonsági másolatokat a megadott tárolóból, amíg a Complete-AzSqlInstanceDatabaseLogReplay meg nem hívjuk a legutóbbi szükséges biztonsági mentéssel.</span><span class="sxs-lookup"><span data-stu-id="d990c-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="d990c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d990c-114">PARAMETERS</span></span>

### <span data-ttu-id="d990c-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="d990c-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="d990c-116">Az a jelző, amely jelzi, hogy a művelet befejezésekor automatikusan be kell-e fejeződni a visszaállítás.</span><span class="sxs-lookup"><span data-stu-id="d990c-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="d990c-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="d990c-117">-Collation</span></span>
<span data-ttu-id="d990c-118">A használt példányadatbázis szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="d990c-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="d990c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d990c-119">-DefaultProfile</span></span>
<span data-ttu-id="d990c-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d990c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d990c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d990c-121">-InputObject</span></span>
<span data-ttu-id="d990c-122">A példány-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d990c-122">The instance database object.</span></span>

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

### <span data-ttu-id="d990c-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d990c-123">-InstanceName</span></span>
<span data-ttu-id="d990c-124">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="d990c-124">The name of the instance.</span></span>

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

### <span data-ttu-id="d990c-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="d990c-125">-LastBackupName</span></span>
<span data-ttu-id="d990c-126">Az utolsó visszaállítható biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="d990c-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="d990c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d990c-127">-Name</span></span>
<span data-ttu-id="d990c-128">A példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d990c-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="d990c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d990c-129">-PassThru</span></span>
<span data-ttu-id="d990c-130">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="d990c-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="d990c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d990c-131">-ResourceGroupName</span></span>
<span data-ttu-id="d990c-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d990c-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="d990c-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="d990c-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="d990c-134">A tároló sas tokenje.</span><span class="sxs-lookup"><span data-stu-id="d990c-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="d990c-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="d990c-135">-StorageContainerUri</span></span>
<span data-ttu-id="d990c-136">A tároló URI-ja.</span><span class="sxs-lookup"><span data-stu-id="d990c-136">The storage container URI.</span></span>

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

### <span data-ttu-id="d990c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d990c-137">-Confirm</span></span>
<span data-ttu-id="d990c-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d990c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d990c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d990c-139">-WhatIf</span></span>
<span data-ttu-id="d990c-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d990c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d990c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d990c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d990c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d990c-142">CommonParameters</span></span>
<span data-ttu-id="d990c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d990c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d990c-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d990c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d990c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d990c-145">INPUTS</span></span>

### <span data-ttu-id="d990c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d990c-146">System.String</span></span>

### <span data-ttu-id="d990c-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d990c-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d990c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d990c-148">OUTPUTS</span></span>

### <span data-ttu-id="d990c-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d990c-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d990c-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d990c-150">NOTES</span></span>

## <span data-ttu-id="d990c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d990c-151">RELATED LINKS</span></span>
