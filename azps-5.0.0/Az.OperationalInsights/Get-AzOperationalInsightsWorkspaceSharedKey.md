---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185926"
---
# <span data-ttu-id="17a2f-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="17a2f-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="17a2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="17a2f-103">A munkaterület megosztott kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="17a2f-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="17a2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17a2f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17a2f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="17a2f-106">A **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmag a munkaterület megosztott kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="17a2f-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="17a2f-107">A billentyűk segítségével a munkaterülethez kapcsolhatók a műveleti tényezők.</span><span class="sxs-lookup"><span data-stu-id="17a2f-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="17a2f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="17a2f-108">EXAMPLES</span></span>

### <span data-ttu-id="17a2f-109">Példa 1: a megosztott kulcsok beolvasása munkaterület nevével</span><span class="sxs-lookup"><span data-stu-id="17a2f-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="17a2f-110">Ez a parancs a MyWorkspace nevű munkaterület megosztott kulcsait kapja meg az ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="17a2f-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="17a2f-111">2. példa: a megosztott kulcsok beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="17a2f-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="17a2f-112">Ez a parancs a MyWorkspace nevű munkaterületet az Get-AzOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet a **Get-AzOperationalInsightsWorkspaceSharedKey** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="17a2f-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="17a2f-113">A parancs a munkaterülethez tartozó megosztott kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="17a2f-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="17a2f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="17a2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a2f-115">-DefaultProfile</span></span>
<span data-ttu-id="17a2f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17a2f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17a2f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17a2f-117">-Name</span></span>
<span data-ttu-id="17a2f-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17a2f-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="17a2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="17a2f-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17a2f-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="17a2f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a2f-121">CommonParameters</span></span>
<span data-ttu-id="17a2f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17a2f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a2f-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a2f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a2f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17a2f-124">INPUTS</span></span>

### <span data-ttu-id="17a2f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="17a2f-125">System.String</span></span>

## <span data-ttu-id="17a2f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17a2f-126">OUTPUTS</span></span>

### <span data-ttu-id="17a2f-127">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="17a2f-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="17a2f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17a2f-128">NOTES</span></span>

## <span data-ttu-id="17a2f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17a2f-129">RELATED LINKS</span></span>

[<span data-ttu-id="17a2f-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="17a2f-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="17a2f-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="17a2f-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


