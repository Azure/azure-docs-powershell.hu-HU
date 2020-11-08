---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184287"
---
# <span data-ttu-id="136e8-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="136e8-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="136e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="136e8-102">SYNOPSIS</span></span>
<span data-ttu-id="136e8-103">Házirend metaadat-erőforrásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="136e8-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="136e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="136e8-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="136e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="136e8-105">DESCRIPTION</span></span>
<span data-ttu-id="136e8-106">A **Get-AzPolicyRemediation** parancsmag minden házirend metaadat-erőforrását vagy egy bizonyos házirend metaadat-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="136e8-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="136e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="136e8-107">EXAMPLES</span></span>

### <span data-ttu-id="136e8-108">Példa 1: a házirend metaadat-erőforrásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="136e8-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="136e8-109">Ez a parancs minden házirend metaadat-erőforrását kinyeri</span><span class="sxs-lookup"><span data-stu-id="136e8-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="136e8-110">2. példa: 10 házirend metaadat-erőforrásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="136e8-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="136e8-111">Ez a parancs 10 házirend metaadat-erőforrásának gyűjteményét kapja</span><span class="sxs-lookup"><span data-stu-id="136e8-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="136e8-112">3. példa: egyetlen házirend metaadat-erőforrásának beszerzése a ' ACF1348 ' névvel</span><span class="sxs-lookup"><span data-stu-id="136e8-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="136e8-113">Ez a parancs egyetlen házirend-metaadat-erőforrást kap a "ACF1348" névvel.</span><span class="sxs-lookup"><span data-stu-id="136e8-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="136e8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="136e8-114">PARAMETERS</span></span>

### <span data-ttu-id="136e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136e8-115">-DefaultProfile</span></span>
<span data-ttu-id="136e8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="136e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="136e8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="136e8-117">-Name</span></span>
<span data-ttu-id="136e8-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="136e8-118">Resource name.</span></span>

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

### <span data-ttu-id="136e8-119">-Top</span><span class="sxs-lookup"><span data-stu-id="136e8-119">-Top</span></span>
<span data-ttu-id="136e8-120">Az eredményül adott házirend metaadat-erőforrásainak maximális száma.</span><span class="sxs-lookup"><span data-stu-id="136e8-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="136e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136e8-121">CommonParameters</span></span>
<span data-ttu-id="136e8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="136e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136e8-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="136e8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136e8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="136e8-124">INPUTS</span></span>

### <span data-ttu-id="136e8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="136e8-125">System.String</span></span>

## <span data-ttu-id="136e8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="136e8-126">OUTPUTS</span></span>

### <span data-ttu-id="136e8-127">Microsoft. Azure. Command. PolicyInsights. models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="136e8-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="136e8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="136e8-128">NOTES</span></span>

## <span data-ttu-id="136e8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="136e8-129">RELATED LINKS</span></span>
