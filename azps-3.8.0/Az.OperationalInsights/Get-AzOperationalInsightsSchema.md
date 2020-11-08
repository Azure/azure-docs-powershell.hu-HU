---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 93c815a330b9ad8fab4f0aa2f31136819a527b7d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017226"
---
# <span data-ttu-id="4f65f-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="4f65f-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="4f65f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f65f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f65f-103">A munkaterülethez társított sémát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4f65f-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="4f65f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f65f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f65f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f65f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f65f-106">A **Get-AzOperationalInsightsSchema** parancsmag azt a sémát adja meg, amely az erőforráscsoport adott munkaterületéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="4f65f-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="4f65f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4f65f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f65f-108">Példa 1: a sémák beszerzése egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="4f65f-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="4f65f-109">Ez a parancs a munkaterülethez társított sémákat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4f65f-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="4f65f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f65f-110">PARAMETERS</span></span>

### <span data-ttu-id="4f65f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f65f-111">-DefaultProfile</span></span>
<span data-ttu-id="4f65f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f65f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f65f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f65f-113">-ResourceGroupName</span></span>
<span data-ttu-id="4f65f-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4f65f-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="4f65f-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f65f-115">-WorkspaceName</span></span>
<span data-ttu-id="4f65f-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f65f-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f65f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f65f-117">CommonParameters</span></span>
<span data-ttu-id="4f65f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f65f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f65f-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f65f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f65f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f65f-120">INPUTS</span></span>

### <span data-ttu-id="4f65f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4f65f-121">System.String</span></span>

## <span data-ttu-id="4f65f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f65f-122">OUTPUTS</span></span>

### <span data-ttu-id="4f65f-123">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="4f65f-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="4f65f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f65f-124">NOTES</span></span>

## <span data-ttu-id="4f65f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f65f-125">RELATED LINKS</span></span>

[<span data-ttu-id="4f65f-126">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4f65f-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


