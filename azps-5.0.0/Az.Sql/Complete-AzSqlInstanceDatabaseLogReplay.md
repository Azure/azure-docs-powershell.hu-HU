---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187000"
---
# <span data-ttu-id="26076-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="26076-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="26076-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26076-102">SYNOPSIS</span></span>
<span data-ttu-id="26076-103">Végrehajtja a naplózási ismétlés szolgáltatást az adott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="26076-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="26076-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26076-104">SYNTAX</span></span>

### <span data-ttu-id="26076-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26076-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26076-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="26076-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26076-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="26076-107">DESCRIPTION</span></span>
<span data-ttu-id="26076-108">A **Complete-AzSqlInstanceDatabaseLogReplay** parancsmag végrehajtja a naplózási ismétlés szolgáltatást a megadott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="26076-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="26076-109">Példák</span><span class="sxs-lookup"><span data-stu-id="26076-109">EXAMPLES</span></span>

### <span data-ttu-id="26076-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26076-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="26076-111">Az utolsó biztonsági másolat visszahívása után a parancs befejezi a naplózást az adott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="26076-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="26076-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26076-112">PARAMETERS</span></span>

### <span data-ttu-id="26076-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26076-113">-DefaultProfile</span></span>
<span data-ttu-id="26076-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26076-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26076-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26076-115">-InputObject</span></span>
<span data-ttu-id="26076-116">A példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="26076-116">The instance database object.</span></span>

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

### <span data-ttu-id="26076-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="26076-117">-InstanceName</span></span>
<span data-ttu-id="26076-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="26076-118">The name of the instance.</span></span>

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

### <span data-ttu-id="26076-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="26076-119">-LastBackupName</span></span>
<span data-ttu-id="26076-120">A visszaállítani kívánt utolsó biztonságimásolat-fájl neve.</span><span class="sxs-lookup"><span data-stu-id="26076-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="26076-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26076-121">-Name</span></span>
<span data-ttu-id="26076-122">A példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="26076-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="26076-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26076-123">-PassThru</span></span>
<span data-ttu-id="26076-124">Meghatározza, hogy a szinkronizálási csoportot adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="26076-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="26076-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26076-125">-ResourceGroupName</span></span>
<span data-ttu-id="26076-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26076-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="26076-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26076-127">-Confirm</span></span>
<span data-ttu-id="26076-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26076-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26076-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26076-129">-WhatIf</span></span>
<span data-ttu-id="26076-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26076-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26076-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26076-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26076-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26076-132">CommonParameters</span></span>
<span data-ttu-id="26076-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26076-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26076-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26076-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26076-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26076-135">INPUTS</span></span>

### <span data-ttu-id="26076-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26076-136">System.String</span></span>

### <span data-ttu-id="26076-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="26076-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="26076-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26076-138">OUTPUTS</span></span>

## <span data-ttu-id="26076-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26076-139">NOTES</span></span>

## <span data-ttu-id="26076-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26076-140">RELATED LINKS</span></span>
