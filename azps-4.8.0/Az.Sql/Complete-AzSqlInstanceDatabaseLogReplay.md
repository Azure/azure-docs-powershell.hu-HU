---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183277"
---
# <span data-ttu-id="e5325-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e5325-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e5325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5325-102">SYNOPSIS</span></span>
<span data-ttu-id="e5325-103">Végrehajtja a naplózási ismétlés szolgáltatást az adott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e5325-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="e5325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5325-104">SYNTAX</span></span>

### <span data-ttu-id="e5325-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5325-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5325-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e5325-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5325-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5325-107">DESCRIPTION</span></span>
<span data-ttu-id="e5325-108">A **Complete-AzSqlInstanceDatabaseLogReplay** parancsmag végrehajtja a naplózási ismétlés szolgáltatást a megadott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="e5325-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="e5325-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5325-109">EXAMPLES</span></span>

### <span data-ttu-id="e5325-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5325-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="e5325-111">Az utolsó biztonsági másolat visszahívása után a parancs befejezi a naplózást az adott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e5325-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="e5325-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5325-112">PARAMETERS</span></span>

### <span data-ttu-id="e5325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5325-113">-DefaultProfile</span></span>
<span data-ttu-id="e5325-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5325-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5325-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5325-115">-InputObject</span></span>
<span data-ttu-id="e5325-116">A példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="e5325-116">The instance database object.</span></span>

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

### <span data-ttu-id="e5325-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="e5325-117">-InstanceName</span></span>
<span data-ttu-id="e5325-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="e5325-118">The name of the instance.</span></span>

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

### <span data-ttu-id="e5325-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="e5325-119">-LastBackupName</span></span>
<span data-ttu-id="e5325-120">A visszaállítani kívánt utolsó biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="e5325-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="e5325-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5325-121">-Name</span></span>
<span data-ttu-id="e5325-122">A példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e5325-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="e5325-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5325-123">-PassThru</span></span>
<span data-ttu-id="e5325-124">Meghatározza, hogy a szinkronizálási csoportot adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="e5325-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e5325-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5325-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5325-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5325-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5325-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5325-127">-Confirm</span></span>
<span data-ttu-id="e5325-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5325-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5325-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5325-129">-WhatIf</span></span>
<span data-ttu-id="e5325-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5325-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5325-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5325-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5325-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5325-132">CommonParameters</span></span>
<span data-ttu-id="e5325-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5325-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5325-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e5325-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5325-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5325-135">INPUTS</span></span>

### <span data-ttu-id="e5325-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e5325-136">System.String</span></span>

### <span data-ttu-id="e5325-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e5325-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e5325-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5325-138">OUTPUTS</span></span>

## <span data-ttu-id="e5325-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5325-139">NOTES</span></span>

## <span data-ttu-id="e5325-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5325-140">RELATED LINKS</span></span>
