---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e4f966d542110f96672857c2222d44ae03d331ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847942"
---
# <span data-ttu-id="ba432-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ba432-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ba432-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba432-102">SYNOPSIS</span></span>
<span data-ttu-id="ba432-103">Tárterület-betekintést hoz létre a munkaterületen belül.</span><span class="sxs-lookup"><span data-stu-id="ba432-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="ba432-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba432-104">SYNTAX</span></span>

### <span data-ttu-id="ba432-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba432-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba432-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ba432-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba432-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba432-107">DESCRIPTION</span></span>
<span data-ttu-id="ba432-108">A **New-AzOperationalInsightsStorageInsight** parancsmag új tárterület-betekintést hoz létre egy meglévő munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ba432-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="ba432-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba432-109">EXAMPLES</span></span>

### <span data-ttu-id="ba432-110">Példa 1: tárterület-betekintést hozhat létre név szerint</span><span class="sxs-lookup"><span data-stu-id="ba432-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="ba432-111">Az első parancs az Get-AzStorageAccount parancsmagot használja a ContosoStorage nevű tárterület-fiók beszerzéséhez, majd a $Storage változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba432-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="ba432-112">A második parancs a tárolási fiókot $Storage a Get-AzStorageAccountKey parancsmagra a pipeline operátorral a megadott tárterület-kulcs beszerzéséhez, majd a $StorageKey változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba432-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="ba432-113">A végleges parancs létrehoz egy MyStorageInsight nevű tárterület-betekintést a MyWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ba432-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="ba432-114">Ez a tárterület-betekintési funkció a megadott WADWindowsEventLogsTable-erőforrásból származó adatot a megadott tárterület-erőforrásból veszi fel.</span><span class="sxs-lookup"><span data-stu-id="ba432-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="ba432-115">2. példa: tárhely-betekintést hozhat létre egy munkaterület-objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="ba432-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="ba432-116">Az első parancs az Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd a $Workspace változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba432-116">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="ba432-117">A második parancs az Get-AzStorageAccount parancsmagot használja a megadott tárterület beszerzéséhez, majd a $Storage változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba432-117">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="ba432-118">A harmadik parancs a tárolási fiókot $Storage a Get-AzStorageAccountKey parancsmagra a csővezeték-kezelő segítségével a megadott kulcs eléréséhez, majd a $StorageKey változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba432-118">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="ba432-119">A végleges parancs létrehoz egy MyStorageInsight nevű tárterület-betekintést a $Workspaceban definiált munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ba432-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="ba432-120">A tárolási betekintési funkció a megadott WADWindowsEventLogsTable-erőforrásból származó adatot a megadott tárterület-erőforrásból veszi fel.</span><span class="sxs-lookup"><span data-stu-id="ba432-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="ba432-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba432-121">PARAMETERS</span></span>

### <span data-ttu-id="ba432-122">-Tárolók</span><span class="sxs-lookup"><span data-stu-id="ba432-122">-Containers</span></span>
<span data-ttu-id="ba432-123">Az adatokat tartalmazó tárolók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="ba432-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba432-124">-DefaultProfile</span></span>
<span data-ttu-id="ba432-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba432-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba432-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ba432-126">-Force</span></span>
<span data-ttu-id="ba432-127">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ba432-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba432-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba432-128">-Name</span></span>
<span data-ttu-id="ba432-129">A tárterület-betekintési terület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="ba432-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba432-130">-ResourceGroupName</span></span>
<span data-ttu-id="ba432-131">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ba432-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ba432-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba432-132">-StorageAccountKey</span></span>
<span data-ttu-id="ba432-133">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="ba432-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ba432-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="ba432-135">A tárolási fiók Azure-erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="ba432-136">Ezt a beolvashatja az Get-AzStorageAccount parancsmag végrehajtásával és az eredmény *azonosító* paraméterének elérésével.</span><span class="sxs-lookup"><span data-stu-id="ba432-136">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="ba432-137">-Tables (táblázatok)</span><span class="sxs-lookup"><span data-stu-id="ba432-137">-Tables</span></span>
<span data-ttu-id="ba432-138">Az adatot szolgáltató táblák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="ba432-139">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="ba432-139">-Workspace</span></span>
<span data-ttu-id="ba432-140">Az új tárterület-betekintési munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="ba432-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba432-141">-WorkspaceName</span></span>
<span data-ttu-id="ba432-142">A meglévő munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba432-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="ba432-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba432-143">-Confirm</span></span>
<span data-ttu-id="ba432-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba432-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba432-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba432-145">-WhatIf</span></span>
<span data-ttu-id="ba432-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba432-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba432-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba432-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba432-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba432-148">CommonParameters</span></span>
<span data-ttu-id="ba432-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba432-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba432-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba432-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba432-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba432-151">INPUTS</span></span>

### <span data-ttu-id="ba432-152">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba432-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ba432-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ba432-153">System.String</span></span>

### <span data-ttu-id="ba432-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="ba432-154">System.String[]</span></span>

## <span data-ttu-id="ba432-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba432-155">OUTPUTS</span></span>

### <span data-ttu-id="ba432-156">Microsoft. Azure. Command. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ba432-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="ba432-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba432-157">NOTES</span></span>

## <span data-ttu-id="ba432-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba432-158">RELATED LINKS</span></span>

[<span data-ttu-id="ba432-159">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba432-159">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="ba432-160">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba432-160">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


