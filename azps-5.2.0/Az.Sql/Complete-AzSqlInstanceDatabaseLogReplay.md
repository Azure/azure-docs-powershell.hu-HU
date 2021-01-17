---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334805"
---
# <span data-ttu-id="d7cc4-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d7cc4-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="d7cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cc4-103">A megadott adatbázis napló-visszajátszási szolgáltatásának befejezése.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="d7cc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7cc4-104">SYNTAX</span></span>

### <span data-ttu-id="d7cc4-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7cc4-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cc4-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d7cc4-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7cc4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7cc4-107">DESCRIPTION</span></span>
<span data-ttu-id="d7cc4-108">A **Complete-AzSqlInstanceDatabaseLogReplay** parancsmag befejezi a Log Replay szolgáltatást a megadott adatbázison.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="d7cc4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7cc4-109">EXAMPLES</span></span>

### <span data-ttu-id="d7cc4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7cc4-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="d7cc4-111">Ez a parancs az utolsó biztonsági mentés visszaállítása után befejezi az adott adatbázis napló-visszajátszási szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="d7cc4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7cc4-112">PARAMETERS</span></span>

### <span data-ttu-id="d7cc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cc4-113">-DefaultProfile</span></span>
<span data-ttu-id="d7cc4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7cc4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7cc4-115">-InputObject</span></span>
<span data-ttu-id="d7cc4-116">A példány-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-116">The instance database object.</span></span>

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

### <span data-ttu-id="d7cc4-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d7cc4-117">-InstanceName</span></span>
<span data-ttu-id="d7cc4-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-118">The name of the instance.</span></span>

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

### <span data-ttu-id="d7cc4-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="d7cc4-119">-LastBackupName</span></span>
<span data-ttu-id="d7cc4-120">Az utolsó visszaállítható biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7cc4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7cc4-121">-Name</span></span>
<span data-ttu-id="d7cc4-122">A példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="d7cc4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7cc4-123">-PassThru</span></span>
<span data-ttu-id="d7cc4-124">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="d7cc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7cc4-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7cc4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7cc4-127">-Confirm</span></span>
<span data-ttu-id="d7cc4-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7cc4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7cc4-129">-WhatIf</span></span>
<span data-ttu-id="d7cc4-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7cc4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7cc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cc4-132">CommonParameters</span></span>
<span data-ttu-id="d7cc4-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7cc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cc4-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7cc4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cc4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7cc4-135">INPUTS</span></span>

### <span data-ttu-id="d7cc4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d7cc4-136">System.String</span></span>

### <span data-ttu-id="d7cc4-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d7cc4-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d7cc4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7cc4-138">OUTPUTS</span></span>

## <span data-ttu-id="d7cc4-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7cc4-139">NOTES</span></span>

## <span data-ttu-id="d7cc4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7cc4-140">RELATED LINKS</span></span>
