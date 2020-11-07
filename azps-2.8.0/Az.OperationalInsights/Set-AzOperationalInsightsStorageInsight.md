---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b81d7e7d87e8db7658db425f889630a3897d1ecd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847934"
---
# <span data-ttu-id="25b02-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="25b02-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="25b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25b02-102">SYNOPSIS</span></span>
<span data-ttu-id="25b02-103">A tárterület-betekintést frissíti.</span><span class="sxs-lookup"><span data-stu-id="25b02-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="25b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25b02-104">SYNTAX</span></span>

### <span data-ttu-id="25b02-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25b02-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25b02-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="25b02-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25b02-107">DESCRIPTION</span></span>
<span data-ttu-id="25b02-108">A **set-AzOperationalInsightsStorageInsight** parancsmag a tárolási Insight konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="25b02-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="25b02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25b02-109">EXAMPLES</span></span>

### <span data-ttu-id="25b02-110">Példa 1: tárterület-betekintés módosítása név szerint</span><span class="sxs-lookup"><span data-stu-id="25b02-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="25b02-111">Ez a parancs módosítja azokat a táblákat, amelyekben a MyStorageInsight felolvasott tárterület-betekintést kapta.</span><span class="sxs-lookup"><span data-stu-id="25b02-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="25b02-112">2. példa: tárterület-betekintés módosítása munkaterületi objektum használatával</span><span class="sxs-lookup"><span data-stu-id="25b02-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="25b02-113">Az első parancs az Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd a $Workspace változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="25b02-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="25b02-114">A második parancs módosítja azokat a tárolókat, amelyekből a MyStorageInsight nevű tárterület-betekintést olvasta.</span><span class="sxs-lookup"><span data-stu-id="25b02-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="25b02-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25b02-115">PARAMETERS</span></span>

### <span data-ttu-id="25b02-116">-Tárolók</span><span class="sxs-lookup"><span data-stu-id="25b02-116">-Containers</span></span>
<span data-ttu-id="25b02-117">Az adatot szolgáltató tárolók listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="25b02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b02-118">-DefaultProfile</span></span>
<span data-ttu-id="25b02-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25b02-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25b02-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25b02-120">-Name</span></span>
<span data-ttu-id="25b02-121">A tárterület-betekintési terület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="25b02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b02-122">-ResourceGroupName</span></span>
<span data-ttu-id="25b02-123">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="25b02-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="25b02-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="25b02-124">-StorageAccountKey</span></span>
<span data-ttu-id="25b02-125">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b02-126">-Tables (táblázatok)</span><span class="sxs-lookup"><span data-stu-id="25b02-126">-Tables</span></span>
<span data-ttu-id="25b02-127">Az adatokat tartalmazó táblák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b02-128">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="25b02-128">-Workspace</span></span>
<span data-ttu-id="25b02-129">A tárterület-betekintést tartalmazó munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="25b02-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="25b02-130">-WorkspaceName</span></span>
<span data-ttu-id="25b02-131">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25b02-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="25b02-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b02-132">CommonParameters</span></span>
<span data-ttu-id="25b02-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25b02-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b02-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b02-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b02-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25b02-135">INPUTS</span></span>

### <span data-ttu-id="25b02-136">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25b02-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="25b02-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25b02-137">System.String</span></span>

### <span data-ttu-id="25b02-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="25b02-138">System.String[]</span></span>

## <span data-ttu-id="25b02-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25b02-139">OUTPUTS</span></span>

### <span data-ttu-id="25b02-140">Microsoft. Azure. Command. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="25b02-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="25b02-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25b02-141">NOTES</span></span>

## <span data-ttu-id="25b02-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25b02-142">RELATED LINKS</span></span>

[<span data-ttu-id="25b02-143">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="25b02-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="25b02-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="25b02-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

