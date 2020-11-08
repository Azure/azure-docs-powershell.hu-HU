---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184735"
---
# <span data-ttu-id="c2963-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="c2963-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="c2963-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2963-102">SYNOPSIS</span></span>
<span data-ttu-id="c2963-103">A munkaterülethez társított sémát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c2963-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="c2963-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2963-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2963-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2963-105">DESCRIPTION</span></span>
<span data-ttu-id="c2963-106">A **Get-AzOperationalInsightsSchema** parancsmag azt a sémát adja meg, amely az erőforráscsoport adott munkaterületéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="c2963-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="c2963-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c2963-107">EXAMPLES</span></span>

### <span data-ttu-id="c2963-108">Példa 1: a sémák beszerzése egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="c2963-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c2963-109">Ez a parancs a munkaterülethez társított sémákat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c2963-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="c2963-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2963-110">PARAMETERS</span></span>

### <span data-ttu-id="c2963-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2963-111">-DefaultProfile</span></span>
<span data-ttu-id="c2963-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2963-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2963-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2963-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2963-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c2963-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c2963-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2963-115">-WorkspaceName</span></span>
<span data-ttu-id="c2963-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2963-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c2963-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2963-117">CommonParameters</span></span>
<span data-ttu-id="c2963-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2963-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2963-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2963-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2963-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2963-120">INPUTS</span></span>

### <span data-ttu-id="c2963-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c2963-121">System.String</span></span>

## <span data-ttu-id="c2963-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2963-122">OUTPUTS</span></span>

### <span data-ttu-id="c2963-123">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="c2963-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="c2963-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2963-124">NOTES</span></span>

## <span data-ttu-id="c2963-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2963-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2963-126">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c2963-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


