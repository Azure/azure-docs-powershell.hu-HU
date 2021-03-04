---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937961"
---
# <span data-ttu-id="2615d-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="2615d-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="2615d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2615d-102">SYNOPSIS</span></span>
<span data-ttu-id="2615d-103">Tárterület-betekintőt hoz létre egy munkaterületen belül.</span><span class="sxs-lookup"><span data-stu-id="2615d-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="2615d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2615d-104">SYNTAX</span></span>

### <span data-ttu-id="2615d-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2615d-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2615d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2615d-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2615d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2615d-107">DESCRIPTION</span></span>
<span data-ttu-id="2615d-108">A **New-AzOperationalInsightsStorageInsight** parancsmag új Tárterület-betekintőt hoz létre egy meglévő munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="2615d-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="2615d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2615d-109">EXAMPLES</span></span>

### <span data-ttu-id="2615d-110">1. példa: Tárterület-betekintés létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="2615d-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="2615d-111">Az első parancs a Get-AzStorageAccount parancsmagot használva szerezze be a ContosoStorage nevű tárfiókot, majd tárolja azt a $Storage változóban.</span><span class="sxs-lookup"><span data-stu-id="2615d-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="2615d-112">A második parancs átadja a $Storage-ban található tárfiókot a Get-AzStorageAccountKey-parancsmagnak úgy, hogy a pipeline operátorral beveszi a megadott tárfiókkulcsot, majd a $StorageKey változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2615d-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="2615d-113">Ez a példa beolvassa az első kulcsot.</span><span class="sxs-lookup"><span data-stu-id="2615d-113">This example retrieves the first key.</span></span> <span data-ttu-id="2615d-114">A másik lekérése az Érték[0] helyett az Érték[1] értéket használja.</span><span class="sxs-lookup"><span data-stu-id="2615d-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="2615d-115">Az utolsó parancs létrehoz egy MyStorageInsight nevű tárterület-látóteret a MyWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="2615d-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="2615d-116">Ez a tárterület-elemzés a megadott tárfiók-erőforrás WADWindowsEventLogsTable táblából származó adatokat használ fel.</span><span class="sxs-lookup"><span data-stu-id="2615d-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="2615d-117">2. példa: Tárterület-rálátás létrehozása munkaterületi objektum használatával</span><span class="sxs-lookup"><span data-stu-id="2615d-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="2615d-118">Az első parancs a Get-AzOperationalInsightsWorkspace parancsmagot használva szerezze be a MyWorkspace nevű munkaterületet, majd tárolja azt a $Workspace változóban.</span><span class="sxs-lookup"><span data-stu-id="2615d-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="2615d-119">A második parancs a Get-AzStorageAccount parancsmag használatával beveszi a megadott tárfiókot, majd a $Storage tárolja.</span><span class="sxs-lookup"><span data-stu-id="2615d-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="2615d-120">A harmadik parancs átadja a $Storage-ban található tárfiókot a Get-AzStorageAccountKey-parancsmagnak úgy, hogy a pipeline operátorral beveszi a megadott kulcsot, majd a $StorageKey változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2615d-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="2615d-121">Ez a példa beolvassa az első kulcsot.</span><span class="sxs-lookup"><span data-stu-id="2615d-121">This example retrieves the first key.</span></span> <span data-ttu-id="2615d-122">A másik lekérése az Érték[0] helyett az Érték[1] értéket használja.</span><span class="sxs-lookup"><span data-stu-id="2615d-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="2615d-123">A végleges parancs létrehozza a MyStorageInsight nevű tárterület-információt a $Workspace.</span><span class="sxs-lookup"><span data-stu-id="2615d-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="2615d-124">A Storage Insight a megadott tárfiók-erőforrás WADWindowsEventLogsTable táblából származó adatokat használ fel.</span><span class="sxs-lookup"><span data-stu-id="2615d-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="2615d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2615d-125">PARAMETERS</span></span>

### <span data-ttu-id="2615d-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="2615d-126">-Containers</span></span>
<span data-ttu-id="2615d-127">Az adatokat tartalmazó tárolók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2615d-128">-DefaultProfile</span></span>
<span data-ttu-id="2615d-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2615d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2615d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="2615d-130">-Force</span></span>
<span data-ttu-id="2615d-131">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2615d-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2615d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2615d-132">-Name</span></span>
<span data-ttu-id="2615d-133">A Tárterület-elemzés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-133">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2615d-134">-ResourceGroupName</span></span>
<span data-ttu-id="2615d-135">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2615d-136">-StorageAccountKey</span></span>
<span data-ttu-id="2615d-137">A tárfiók hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2615d-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="2615d-139">Egy tárfiók Azure-erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="2615d-140">Ez a lekérdezés a Get-AzStorageAccount futtatásával és az eredmény azonosító  paraméterének elérésével szerezhető be.</span><span class="sxs-lookup"><span data-stu-id="2615d-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-141">-Tables</span><span class="sxs-lookup"><span data-stu-id="2615d-141">-Tables</span></span>
<span data-ttu-id="2615d-142">Megadja az adatokat szolgáltató táblák listáját.</span><span class="sxs-lookup"><span data-stu-id="2615d-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-143">-Workspace</span><span class="sxs-lookup"><span data-stu-id="2615d-143">-Workspace</span></span>
<span data-ttu-id="2615d-144">Az új Tárterület-elemzés munkaterületét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-144">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2615d-145">-WorkspaceName</span></span>
<span data-ttu-id="2615d-146">Egy meglévő munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2615d-146">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2615d-147">-Confirm</span></span>
<span data-ttu-id="2615d-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2615d-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2615d-149">-WhatIf</span></span>
<span data-ttu-id="2615d-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2615d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2615d-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2615d-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2615d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2615d-152">CommonParameters</span></span>
<span data-ttu-id="2615d-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2615d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2615d-154">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2615d-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2615d-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2615d-155">INPUTS</span></span>

### <span data-ttu-id="2615d-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2615d-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2615d-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2615d-157">System.String</span></span>

### <span data-ttu-id="2615d-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2615d-158">System.String[]</span></span>

## <span data-ttu-id="2615d-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2615d-159">OUTPUTS</span></span>

### <span data-ttu-id="2615d-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="2615d-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="2615d-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2615d-161">NOTES</span></span>

## <span data-ttu-id="2615d-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2615d-162">RELATED LINKS</span></span>

[<span data-ttu-id="2615d-163">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2615d-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="2615d-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2615d-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


