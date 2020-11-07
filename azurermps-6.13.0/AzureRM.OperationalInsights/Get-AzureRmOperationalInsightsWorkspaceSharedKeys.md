---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 07d0834b89010ff533e1620f29904ea159d3dfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679839"
---
# <span data-ttu-id="3f24e-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="3f24e-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="3f24e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f24e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f24e-103">A munkaterület megosztott kulcsait kapja.</span><span class="sxs-lookup"><span data-stu-id="3f24e-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f24e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f24e-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f24e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f24e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f24e-106">A **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** parancsmag a munkaterület megosztott kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="3f24e-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="3f24e-107">A billentyűk segítségével a munkaterülethez kapcsolhatók a műveleti tényezők.</span><span class="sxs-lookup"><span data-stu-id="3f24e-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="3f24e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3f24e-108">EXAMPLES</span></span>

### <span data-ttu-id="3f24e-109">Példa 1: a megosztott kulcsok beolvasása munkaterület nevével</span><span class="sxs-lookup"><span data-stu-id="3f24e-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="3f24e-110">Ez a parancs a MyWorkspace nevű munkaterület megosztott kulcsait kapja meg az ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="3f24e-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="3f24e-111">2. példa: a megosztott kulcsok beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="3f24e-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="3f24e-112">Ez a parancs a MyWorkspace nevű munkaterületet az Get-AzureRmOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet a **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="3f24e-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="3f24e-113">A parancs a munkaterülethez tartozó megosztott kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3f24e-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="3f24e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f24e-114">PARAMETERS</span></span>

### <span data-ttu-id="3f24e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f24e-115">-DefaultProfile</span></span>
<span data-ttu-id="3f24e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f24e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f24e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f24e-117">-Name</span></span>
<span data-ttu-id="3f24e-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f24e-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3f24e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f24e-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f24e-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f24e-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="3f24e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f24e-121">CommonParameters</span></span>
<span data-ttu-id="3f24e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f24e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f24e-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f24e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f24e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f24e-124">INPUTS</span></span>

### <span data-ttu-id="3f24e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3f24e-125">System.String</span></span>

## <span data-ttu-id="3f24e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f24e-126">OUTPUTS</span></span>

### <span data-ttu-id="3f24e-127">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="3f24e-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="3f24e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f24e-128">NOTES</span></span>

## <span data-ttu-id="3f24e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f24e-129">RELATED LINKS</span></span>

[<span data-ttu-id="3f24e-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3f24e-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="3f24e-131">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f24e-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


