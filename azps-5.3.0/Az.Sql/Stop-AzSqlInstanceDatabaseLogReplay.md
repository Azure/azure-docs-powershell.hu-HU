---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468005"
---
# <span data-ttu-id="9c672-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9c672-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9c672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c672-102">SYNOPSIS</span></span>
<span data-ttu-id="9c672-103">Megszakítja a Napló visszajátszása szolgáltatást az adatbázis leejtésében.</span><span class="sxs-lookup"><span data-stu-id="9c672-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="9c672-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c672-104">SYNTAX</span></span>

### <span data-ttu-id="9c672-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c672-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c672-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9c672-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c672-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c672-107">DESCRIPTION</span></span>
<span data-ttu-id="9c672-108">A **Stop-AzSqlInstanceDatabaseLogReplay** parancsmag leállítja az adatbázist, és így megszakítja a Log Replay szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="9c672-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="9c672-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c672-109">EXAMPLES</span></span>

### <span data-ttu-id="9c672-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c672-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="9c672-111">Ez a parancs megszakítja a napló-visszajátszási szolgáltatást az adott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="9c672-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="9c672-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c672-112">PARAMETERS</span></span>

### <span data-ttu-id="9c672-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c672-113">-DefaultProfile</span></span>
<span data-ttu-id="9c672-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c672-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c672-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9c672-115">-Force</span></span>
<span data-ttu-id="9c672-116">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="9c672-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9c672-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c672-117">-InputObject</span></span>
<span data-ttu-id="9c672-118">A példány-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="9c672-118">The instance database object.</span></span>

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

### <span data-ttu-id="9c672-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9c672-119">-InstanceName</span></span>
<span data-ttu-id="9c672-120">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="9c672-120">The name of the instance.</span></span>

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

### <span data-ttu-id="9c672-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9c672-121">-Name</span></span>
<span data-ttu-id="9c672-122">A példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9c672-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="9c672-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c672-123">-PassThru</span></span>
<span data-ttu-id="9c672-124">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="9c672-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="9c672-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c672-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c672-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c672-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c672-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c672-127">-Confirm</span></span>
<span data-ttu-id="9c672-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c672-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c672-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c672-129">-WhatIf</span></span>
<span data-ttu-id="9c672-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c672-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c672-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c672-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c672-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c672-132">CommonParameters</span></span>
<span data-ttu-id="9c672-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c672-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c672-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c672-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c672-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c672-135">INPUTS</span></span>

### <span data-ttu-id="9c672-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9c672-136">System.String</span></span>

### <span data-ttu-id="9c672-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9c672-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9c672-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c672-138">OUTPUTS</span></span>

### <span data-ttu-id="9c672-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9c672-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9c672-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c672-140">NOTES</span></span>

## <span data-ttu-id="9c672-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c672-141">RELATED LINKS</span></span>
