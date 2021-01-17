---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470098"
---
# <span data-ttu-id="26f24-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="26f24-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="26f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f24-102">SYNOPSIS</span></span>
<span data-ttu-id="26f24-103">Engedélyezi vagy letiltja a megadott intelligensintelligencia-csomagot.</span><span class="sxs-lookup"><span data-stu-id="26f24-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="26f24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26f24-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f24-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26f24-105">DESCRIPTION</span></span>
<span data-ttu-id="26f24-106">A **Set-AzOperationalInsightsIntelligencePack** parancsmag engedélyezi a megadott intelligensintelligencia-csomagot, ha az *Engedélyezve* beállítás $True, és letiltja, ha az *Engedélyezve* beállítás $False.</span><span class="sxs-lookup"><span data-stu-id="26f24-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="26f24-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26f24-107">EXAMPLES</span></span>

### <span data-ttu-id="26f24-108">1. példa: Intelligens csomagok beállítása</span><span class="sxs-lookup"><span data-stu-id="26f24-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="26f24-109">Ez a parancs engedélyezi a megadott intelligensintelligencia-csomagot.</span><span class="sxs-lookup"><span data-stu-id="26f24-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="26f24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26f24-110">PARAMETERS</span></span>

### <span data-ttu-id="26f24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f24-111">-DefaultProfile</span></span>
<span data-ttu-id="26f24-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="26f24-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26f24-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="26f24-113">-Enabled</span></span>
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

### <span data-ttu-id="26f24-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="26f24-114">-IntelligencePackName</span></span>
<span data-ttu-id="26f24-115">Az intelligenciacsomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26f24-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="26f24-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f24-116">-ResourceGroupName</span></span>
<span data-ttu-id="26f24-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26f24-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="26f24-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26f24-118">-WorkspaceName</span></span>
<span data-ttu-id="26f24-119">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26f24-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="26f24-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f24-120">CommonParameters</span></span>
<span data-ttu-id="26f24-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f24-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f24-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f24-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f24-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26f24-123">INPUTS</span></span>

### <span data-ttu-id="26f24-124">System.String</span><span class="sxs-lookup"><span data-stu-id="26f24-124">System.String</span></span>

### <span data-ttu-id="26f24-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26f24-125">System.Boolean</span></span>

## <span data-ttu-id="26f24-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f24-126">OUTPUTS</span></span>

### <span data-ttu-id="26f24-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="26f24-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="26f24-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26f24-128">NOTES</span></span>

## <span data-ttu-id="26f24-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26f24-129">RELATED LINKS</span></span>

[<span data-ttu-id="26f24-130">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="26f24-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


