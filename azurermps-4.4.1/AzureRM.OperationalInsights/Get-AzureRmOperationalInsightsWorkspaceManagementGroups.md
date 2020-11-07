---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 55fe1a82d0e54606c04954167aef2c2b90086655
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679375"
---
# <span data-ttu-id="eef19-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="eef19-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="eef19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eef19-102">SYNOPSIS</span></span>
<span data-ttu-id="eef19-103">A munkaterülethez kapcsolt felügyeleti csoportok részletes adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eef19-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eef19-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eef19-105">DESCRIPTION</span></span>
<span data-ttu-id="eef19-106">A **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** parancsmag a munkaterülethez kapcsolt felügyeleti csoportokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="eef19-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="eef19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eef19-107">EXAMPLES</span></span>

### <span data-ttu-id="eef19-108">1. példa: felügyeleti csoportok beolvasása munkaterület szerint</span><span class="sxs-lookup"><span data-stu-id="eef19-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="eef19-109">Ez a parancs a MyWorkspace nevű munkaterület felügyeleti csoportját kapja meg az ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="eef19-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="eef19-110">2. példa: felügyeleti csoportok beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="eef19-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="eef19-111">Ez a parancs a Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd átadja a munkaterületet az aktuális parancsmagnak, amely az adott munkaterület kezelési csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="eef19-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="eef19-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eef19-112">PARAMETERS</span></span>

### <span data-ttu-id="eef19-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eef19-113">-Name</span></span>
<span data-ttu-id="eef19-114">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eef19-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="eef19-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef19-115">-ResourceGroupName</span></span>
<span data-ttu-id="eef19-116">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eef19-116">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="eef19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef19-117">-DefaultProfile</span></span>
<span data-ttu-id="eef19-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eef19-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef19-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef19-119">CommonParameters</span></span>
<span data-ttu-id="eef19-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eef19-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef19-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef19-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef19-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef19-122">INPUTS</span></span>

## <span data-ttu-id="eef19-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef19-123">OUTPUTS</span></span>

### <span data-ttu-id="eef19-124">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. models. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="eef19-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="eef19-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eef19-125">NOTES</span></span>

## <span data-ttu-id="eef19-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eef19-126">RELATED LINKS</span></span>

[<span data-ttu-id="eef19-127">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="eef19-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="eef19-128">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eef19-128">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


