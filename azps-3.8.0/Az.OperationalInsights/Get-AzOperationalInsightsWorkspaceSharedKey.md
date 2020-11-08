---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 012d145baf3544eec05de567eadaec82efdb7eae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017276"
---
# <span data-ttu-id="8b237-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="8b237-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="8b237-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b237-102">SYNOPSIS</span></span>
<span data-ttu-id="8b237-103">A munkaterület megosztott kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="8b237-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="8b237-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b237-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b237-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b237-105">DESCRIPTION</span></span>
<span data-ttu-id="8b237-106">A **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmag a munkaterület megosztott kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8b237-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="8b237-107">A billentyűk segítségével a munkaterülethez kapcsolhatók a műveleti tényezők.</span><span class="sxs-lookup"><span data-stu-id="8b237-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="8b237-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8b237-108">EXAMPLES</span></span>

### <span data-ttu-id="8b237-109">Példa 1: a megosztott kulcsok beolvasása munkaterület nevével</span><span class="sxs-lookup"><span data-stu-id="8b237-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="8b237-110">Ez a parancs a MyWorkspace nevű munkaterület megosztott kulcsait kapja meg az ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="8b237-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8b237-111">2. példa: a megosztott kulcsok beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="8b237-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="8b237-112">Ez a parancs a MyWorkspace nevű munkaterületet az Get-AzOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet a **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8b237-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="8b237-113">A parancs a munkaterülethez tartozó megosztott kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b237-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="8b237-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b237-114">PARAMETERS</span></span>

### <span data-ttu-id="8b237-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b237-115">-DefaultProfile</span></span>
<span data-ttu-id="8b237-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8b237-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b237-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b237-117">-Name</span></span>
<span data-ttu-id="8b237-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b237-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="8b237-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b237-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b237-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b237-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8b237-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b237-121">CommonParameters</span></span>
<span data-ttu-id="8b237-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b237-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b237-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b237-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b237-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b237-124">INPUTS</span></span>

### <span data-ttu-id="8b237-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8b237-125">System.String</span></span>

## <span data-ttu-id="8b237-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b237-126">OUTPUTS</span></span>

### <span data-ttu-id="8b237-127">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="8b237-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="8b237-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b237-128">NOTES</span></span>

## <span data-ttu-id="8b237-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b237-129">RELATED LINKS</span></span>

[<span data-ttu-id="8b237-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8b237-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="8b237-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b237-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


