---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339894"
---
# <span data-ttu-id="a3547-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="a3547-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="a3547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3547-102">SYNOPSIS</span></span>
<span data-ttu-id="a3547-103">A munkaterület megosztott kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a3547-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="a3547-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3547-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3547-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3547-105">DESCRIPTION</span></span>
<span data-ttu-id="a3547-106">A **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmag felsorolja a munkaterületek megosztott kulcsait.</span><span class="sxs-lookup"><span data-stu-id="a3547-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="a3547-107">A kulcsokkal a Műveleti betekintések ügynökeit csatlakoztathatja a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="a3547-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="a3547-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3547-108">EXAMPLES</span></span>

### <span data-ttu-id="a3547-109">1. példa: Megosztott kulcsok lekérte munkaterület neve alapján</span><span class="sxs-lookup"><span data-stu-id="a3547-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a3547-110">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport MyWorkspace nevű munkaterületének megosztott kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a3547-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a3547-111">2. példa: Megosztott kulcsok lekérte a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="a3547-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="a3547-112">Ez a parancs a MyWorkspace nevű munkaterületet a Get-AzOperationalInsightsWorkspace-parancsmag használatával kapja meg, majd átadja a munkaterületet a **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a3547-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="a3547-113">A parancs a munkaterület megosztott kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a3547-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="a3547-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3547-114">PARAMETERS</span></span>

### <span data-ttu-id="a3547-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3547-115">-DefaultProfile</span></span>
<span data-ttu-id="a3547-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3547-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3547-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a3547-117">-Name</span></span>
<span data-ttu-id="a3547-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3547-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3547-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3547-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3547-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3547-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3547-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3547-121">CommonParameters</span></span>
<span data-ttu-id="a3547-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3547-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3547-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3547-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3547-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3547-124">INPUTS</span></span>

### <span data-ttu-id="a3547-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a3547-125">System.String</span></span>

## <span data-ttu-id="a3547-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3547-126">OUTPUTS</span></span>

### <span data-ttu-id="a3547-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="a3547-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="a3547-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3547-128">NOTES</span></span>

## <span data-ttu-id="a3547-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3547-129">RELATED LINKS</span></span>

[<span data-ttu-id="a3547-130">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a3547-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a3547-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3547-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


