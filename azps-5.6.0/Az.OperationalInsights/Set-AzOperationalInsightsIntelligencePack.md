---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937866"
---
# <span data-ttu-id="b5ab5-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b5ab5-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="b5ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ab5-103">Engedélyezi vagy letiltja a megadott intelligensintelligencia-csomagot.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="b5ab5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5ab5-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ab5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ab5-106">A **Set-AzOperationalInsightsIntelligencePack** parancsmag engedélyezi a megadott intelligensintelligencia-csomagot, ha az *Engedélyezve* $True, és letiltja, ha az *Engedélyezve* beállítás $False.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="b5ab5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ab5-108">1. példa: Intelligens csomagok beállítása</span><span class="sxs-lookup"><span data-stu-id="b5ab5-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="b5ab5-109">Ez a parancs engedélyezi a megadott intelligensintelligencia-csomagot.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="b5ab5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ab5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ab5-111">-DefaultProfile</span></span>
<span data-ttu-id="b5ab5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5ab5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5ab5-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b5ab5-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ab5-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="b5ab5-114">-IntelligencePackName</span></span>
<span data-ttu-id="b5ab5-115">Az intelligenciacsomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ab5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ab5-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5ab5-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="b5ab5-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5ab5-118">-WorkspaceName</span></span>
<span data-ttu-id="b5ab5-119">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="b5ab5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ab5-120">CommonParameters</span></span>
<span data-ttu-id="b5ab5-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ab5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ab5-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ab5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ab5-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5ab5-123">INPUTS</span></span>

### <span data-ttu-id="b5ab5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b5ab5-124">System.String</span></span>

### <span data-ttu-id="b5ab5-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5ab5-125">System.Boolean</span></span>

## <span data-ttu-id="b5ab5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ab5-126">OUTPUTS</span></span>

### <span data-ttu-id="b5ab5-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b5ab5-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="b5ab5-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5ab5-128">NOTES</span></span>

## <span data-ttu-id="b5ab5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5ab5-129">RELATED LINKS</span></span>

[<span data-ttu-id="b5ab5-130">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b5ab5-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


