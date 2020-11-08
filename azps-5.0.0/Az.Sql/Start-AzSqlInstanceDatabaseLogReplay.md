---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185648"
---
# <span data-ttu-id="fd165-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="fd165-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="fd165-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd165-102">SYNOPSIS</span></span>
<span data-ttu-id="fd165-103">A megadott paraméterekkel indítja el a napló ismétlése szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="fd165-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="fd165-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd165-104">SYNTAX</span></span>

### <span data-ttu-id="fd165-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd165-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd165-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fd165-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd165-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd165-107">DESCRIPTION</span></span>
<span data-ttu-id="fd165-108">A **Start-AzSqlInstanceDatabaseLogReplay** parancsmag a naplózási ismétlési szolgáltatás indítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="fd165-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="fd165-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fd165-109">EXAMPLES</span></span>

### <span data-ttu-id="fd165-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd165-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="fd165-111">Ez a parancs új felügyelt adatbázist hoz létre, és megkezdi a biztonsági másolatok visszaállítását az adott tárolóról mindaddig, amíg a last_backup. bak vissza nem jelenik.</span><span class="sxs-lookup"><span data-stu-id="fd165-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="fd165-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd165-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="fd165-113">Ez a parancs új felügyelt adatbázist hoz létre, és megkezdi a biztonsági másolatok visszaállítását az adott tárolóról mindaddig, amíg a program az utolsó biztonsági mentést nem kéri Complete-AzSqlInstanceDatabaseLogReplay.</span><span class="sxs-lookup"><span data-stu-id="fd165-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="fd165-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd165-114">PARAMETERS</span></span>

### <span data-ttu-id="fd165-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="fd165-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="fd165-116">Annak jelzése, hogy a befejezéshez az automatikus helyreállítást szeretné-e végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="fd165-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="fd165-117">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="fd165-117">-Collation</span></span>
<span data-ttu-id="fd165-118">A használandó példány-adatbázis egybevetése.</span><span class="sxs-lookup"><span data-stu-id="fd165-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="fd165-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd165-119">-DefaultProfile</span></span>
<span data-ttu-id="fd165-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd165-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd165-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd165-121">-InputObject</span></span>
<span data-ttu-id="fd165-122">A példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="fd165-122">The instance database object.</span></span>

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

### <span data-ttu-id="fd165-123">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="fd165-123">-InstanceName</span></span>
<span data-ttu-id="fd165-124">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="fd165-124">The name of the instance.</span></span>

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

### <span data-ttu-id="fd165-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="fd165-125">-LastBackupName</span></span>
<span data-ttu-id="fd165-126">A visszaállítani kívánt utolsó biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="fd165-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="fd165-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd165-127">-Name</span></span>
<span data-ttu-id="fd165-128">A példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fd165-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="fd165-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd165-129">-PassThru</span></span>
<span data-ttu-id="fd165-130">Meghatározza, hogy a szinkronizálási csoportot adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="fd165-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="fd165-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd165-131">-ResourceGroupName</span></span>
<span data-ttu-id="fd165-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd165-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd165-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="fd165-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="fd165-134">A Storage Container sas-tokenje.</span><span class="sxs-lookup"><span data-stu-id="fd165-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="fd165-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="fd165-135">-StorageContainerUri</span></span>
<span data-ttu-id="fd165-136">A tárterület-tároló URI-ja.</span><span class="sxs-lookup"><span data-stu-id="fd165-136">The storage container URI.</span></span>

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

### <span data-ttu-id="fd165-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd165-137">-Confirm</span></span>
<span data-ttu-id="fd165-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd165-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd165-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd165-139">-WhatIf</span></span>
<span data-ttu-id="fd165-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd165-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd165-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd165-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd165-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd165-142">CommonParameters</span></span>
<span data-ttu-id="fd165-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd165-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd165-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fd165-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd165-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd165-145">INPUTS</span></span>

### <span data-ttu-id="fd165-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fd165-146">System.String</span></span>

### <span data-ttu-id="fd165-147">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fd165-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fd165-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd165-148">OUTPUTS</span></span>

### <span data-ttu-id="fd165-149">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fd165-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fd165-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd165-150">NOTES</span></span>

## <span data-ttu-id="fd165-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd165-151">RELATED LINKS</span></span>
