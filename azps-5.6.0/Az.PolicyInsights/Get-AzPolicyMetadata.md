---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937530"
---
# <span data-ttu-id="ed0e9-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="ed0e9-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="ed0e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0e9-103">Házirend metaadat-erőforrásainak lekérte</span><span class="sxs-lookup"><span data-stu-id="ed0e9-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="ed0e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed0e9-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed0e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0e9-106">A **Get-AzPolicyRemediation** parancsmag begyűjte az összes házirend metaadat-erőforrását vagy egy adott házirend metaadat-erőforrását.</span><span class="sxs-lookup"><span data-stu-id="ed0e9-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="ed0e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0e9-108">1. példa: Az összes házirend metaadat-erőforrásának lekérte</span><span class="sxs-lookup"><span data-stu-id="ed0e9-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="ed0e9-109">Ez a parancs az összes házirend metaadat-erőforrását beveszi</span><span class="sxs-lookup"><span data-stu-id="ed0e9-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="ed0e9-110">2. példa: 10 házirend metaadat-erőforrásának gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="ed0e9-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="ed0e9-111">Ez a parancs 10 házirend metaadat-erőforrásból álló gyűjteményt kap</span><span class="sxs-lookup"><span data-stu-id="ed0e9-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="ed0e9-112">3. példa: Egyetlen házirend metaadat-erőforrásának lekértése "ACF1348" néven</span><span class="sxs-lookup"><span data-stu-id="ed0e9-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="ed0e9-113">Ez a parancs egyetlen házirend metaadat-erőforrást kap "ACF1348" néven</span><span class="sxs-lookup"><span data-stu-id="ed0e9-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="ed0e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed0e9-114">PARAMETERS</span></span>

### <span data-ttu-id="ed0e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0e9-115">-DefaultProfile</span></span>
<span data-ttu-id="ed0e9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed0e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0e9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed0e9-117">-Name</span></span>
<span data-ttu-id="ed0e9-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ed0e9-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0e9-119">-Top</span><span class="sxs-lookup"><span data-stu-id="ed0e9-119">-Top</span></span>
<span data-ttu-id="ed0e9-120">A vissza nem térhet házirend metaadat-erőforrásainak maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ed0e9-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0e9-121">CommonParameters</span></span>
<span data-ttu-id="ed0e9-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0e9-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed0e9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0e9-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed0e9-124">INPUTS</span></span>

### <span data-ttu-id="ed0e9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ed0e9-125">System.String</span></span>

## <span data-ttu-id="ed0e9-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed0e9-126">OUTPUTS</span></span>

### <span data-ttu-id="ed0e9-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="ed0e9-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="ed0e9-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed0e9-128">NOTES</span></span>

## <span data-ttu-id="ed0e9-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed0e9-129">RELATED LINKS</span></span>
