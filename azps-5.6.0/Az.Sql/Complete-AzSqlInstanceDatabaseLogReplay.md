---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2237522cbf7b179358ea4fa9f7ed7608222782ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011574"
---
# <span data-ttu-id="d1edd-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d1edd-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="d1edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1edd-102">SYNOPSIS</span></span>
<span data-ttu-id="d1edd-103">A megadott adatbázis napló-visszajátszási szolgáltatásának befejezése.</span><span class="sxs-lookup"><span data-stu-id="d1edd-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="d1edd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1edd-104">SYNTAX</span></span>

### <span data-ttu-id="d1edd-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1edd-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1edd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d1edd-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1edd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1edd-107">DESCRIPTION</span></span>
<span data-ttu-id="d1edd-108">A **Complete-AzSqlInstanceDatabaseLogReplay** parancsmag befejezi a Log Replay szolgáltatást a megadott adatbázison.</span><span class="sxs-lookup"><span data-stu-id="d1edd-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="d1edd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1edd-109">EXAMPLES</span></span>

### <span data-ttu-id="d1edd-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d1edd-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="d1edd-111">Ez a parancs az utolsó biztonsági mentés visszaállítása után befejezi az adott adatbázis napló-visszajátszási szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="d1edd-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="d1edd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1edd-112">PARAMETERS</span></span>

### <span data-ttu-id="d1edd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1edd-113">-DefaultProfile</span></span>
<span data-ttu-id="d1edd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1edd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1edd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1edd-115">-InputObject</span></span>
<span data-ttu-id="d1edd-116">A példány-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d1edd-116">The instance database object.</span></span>

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

### <span data-ttu-id="d1edd-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1edd-117">-InstanceName</span></span>
<span data-ttu-id="d1edd-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="d1edd-118">The name of the instance.</span></span>

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

### <span data-ttu-id="d1edd-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="d1edd-119">-LastBackupName</span></span>
<span data-ttu-id="d1edd-120">Az utolsó visszaállítható biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="d1edd-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="d1edd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d1edd-121">-Name</span></span>
<span data-ttu-id="d1edd-122">A példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d1edd-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="d1edd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1edd-123">-PassThru</span></span>
<span data-ttu-id="d1edd-124">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="d1edd-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="d1edd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1edd-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1edd-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d1edd-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1edd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1edd-127">-Confirm</span></span>
<span data-ttu-id="d1edd-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d1edd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1edd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1edd-129">-WhatIf</span></span>
<span data-ttu-id="d1edd-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d1edd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1edd-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1edd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1edd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1edd-132">CommonParameters</span></span>
<span data-ttu-id="d1edd-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1edd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1edd-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1edd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1edd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1edd-135">INPUTS</span></span>

### <span data-ttu-id="d1edd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d1edd-136">System.String</span></span>

### <span data-ttu-id="d1edd-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d1edd-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d1edd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1edd-138">OUTPUTS</span></span>

## <span data-ttu-id="d1edd-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1edd-139">NOTES</span></span>

## <span data-ttu-id="d1edd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1edd-140">RELATED LINKS</span></span>
