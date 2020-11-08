---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181291"
---
# <span data-ttu-id="29a12-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="29a12-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="29a12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29a12-102">SYNOPSIS</span></span>
<span data-ttu-id="29a12-103">Lemondhatja a naplózási ismétlési szolgáltatást az adatbázis eldobásával.</span><span class="sxs-lookup"><span data-stu-id="29a12-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="29a12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29a12-104">SYNTAX</span></span>

### <span data-ttu-id="29a12-105">LogReplayInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29a12-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29a12-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="29a12-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29a12-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29a12-107">DESCRIPTION</span></span>
<span data-ttu-id="29a12-108">A **stop-AzSqlInstanceDatabaseLogReplay** parancsmag leesik az adatbázisból, és így megszünteti a naplózási ismétlés szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="29a12-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="29a12-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29a12-109">EXAMPLES</span></span>

### <span data-ttu-id="29a12-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29a12-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="29a12-111">Ez a parancs a megadott adatbázis naplózási ismétlési szolgáltatását fogja lemondani.</span><span class="sxs-lookup"><span data-stu-id="29a12-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="29a12-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29a12-112">PARAMETERS</span></span>

### <span data-ttu-id="29a12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a12-113">-DefaultProfile</span></span>
<span data-ttu-id="29a12-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29a12-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a12-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29a12-115">-Force</span></span>
<span data-ttu-id="29a12-116">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="29a12-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="29a12-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29a12-117">-InputObject</span></span>
<span data-ttu-id="29a12-118">A példány adatbázis-objektuma.</span><span class="sxs-lookup"><span data-stu-id="29a12-118">The instance database object.</span></span>

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

### <span data-ttu-id="29a12-119">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="29a12-119">-InstanceName</span></span>
<span data-ttu-id="29a12-120">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="29a12-120">The name of the instance.</span></span>

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

### <span data-ttu-id="29a12-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29a12-121">-Name</span></span>
<span data-ttu-id="29a12-122">A példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="29a12-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="29a12-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29a12-123">-PassThru</span></span>
<span data-ttu-id="29a12-124">Meghatározza, hogy a szinkronizálási csoportot adja-e vissza.</span><span class="sxs-lookup"><span data-stu-id="29a12-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="29a12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a12-125">-ResourceGroupName</span></span>
<span data-ttu-id="29a12-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="29a12-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="29a12-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29a12-127">-Confirm</span></span>
<span data-ttu-id="29a12-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29a12-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29a12-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29a12-129">-WhatIf</span></span>
<span data-ttu-id="29a12-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29a12-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29a12-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29a12-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29a12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a12-132">CommonParameters</span></span>
<span data-ttu-id="29a12-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29a12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a12-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29a12-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a12-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a12-135">INPUTS</span></span>

### <span data-ttu-id="29a12-136">System. String</span><span class="sxs-lookup"><span data-stu-id="29a12-136">System.String</span></span>

### <span data-ttu-id="29a12-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="29a12-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="29a12-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29a12-138">OUTPUTS</span></span>

### <span data-ttu-id="29a12-139">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="29a12-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="29a12-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29a12-140">NOTES</span></span>

## <span data-ttu-id="29a12-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29a12-141">RELATED LINKS</span></span>
