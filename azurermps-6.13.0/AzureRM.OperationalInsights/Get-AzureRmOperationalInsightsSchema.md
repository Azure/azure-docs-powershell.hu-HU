---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 0dcac3fac32094cf2d9a0e42abcffd6222783e78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498236"
---
# <span data-ttu-id="93a2b-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="93a2b-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="93a2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="93a2b-103">A munkaterülethez társított sémát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="93a2b-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93a2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93a2b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a2b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="93a2b-106">A **Get-AzureRmOperationalInsightsSchema** parancsmag azt a sémát adja meg, amely az erőforráscsoport adott munkaterületéhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="93a2b-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="93a2b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="93a2b-108">Példa 1: a sémák beszerzése egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="93a2b-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="93a2b-109">Ez a parancs a munkaterülethez társított sémákat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="93a2b-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="93a2b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93a2b-110">PARAMETERS</span></span>

### <span data-ttu-id="93a2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a2b-111">-DefaultProfile</span></span>
<span data-ttu-id="93a2b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="93a2b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93a2b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a2b-113">-ResourceGroupName</span></span>
<span data-ttu-id="93a2b-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="93a2b-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="93a2b-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="93a2b-115">-WorkspaceName</span></span>
<span data-ttu-id="93a2b-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93a2b-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="93a2b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a2b-117">CommonParameters</span></span>
<span data-ttu-id="93a2b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93a2b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a2b-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a2b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a2b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93a2b-120">INPUTS</span></span>

### <span data-ttu-id="93a2b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="93a2b-121">System.String</span></span>

## <span data-ttu-id="93a2b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93a2b-122">OUTPUTS</span></span>

### <span data-ttu-id="93a2b-123">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="93a2b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="93a2b-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93a2b-124">NOTES</span></span>

## <span data-ttu-id="93a2b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93a2b-125">RELATED LINKS</span></span>

[<span data-ttu-id="93a2b-126">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="93a2b-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


