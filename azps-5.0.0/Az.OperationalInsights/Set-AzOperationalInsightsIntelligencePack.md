---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186385"
---
# <span data-ttu-id="0a94b-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="0a94b-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="0a94b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a94b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a94b-103">Engedélyezi vagy letiltja a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="0a94b-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="0a94b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a94b-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a94b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a94b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a94b-106">A **set-AzOperationalInsightsIntelligencePack** parancsmag lehetővé teszi a megadott intelligencia-csomag beállítását, ha be van *kapcsolva* a $True, és letiltja azt, ha az *engedélyezve* beállítás értéke $false.</span><span class="sxs-lookup"><span data-stu-id="0a94b-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="0a94b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a94b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a94b-108">1. példa: a hírszerzési csomagok beállítása</span><span class="sxs-lookup"><span data-stu-id="0a94b-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="0a94b-109">Ez a parancs engedélyezi a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="0a94b-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="0a94b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a94b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a94b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a94b-111">-DefaultProfile</span></span>
<span data-ttu-id="0a94b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a94b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a94b-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="0a94b-113">-Enabled</span></span>
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

### <span data-ttu-id="0a94b-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="0a94b-114">-IntelligencePackName</span></span>
<span data-ttu-id="0a94b-115">A hírszerzési csomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a94b-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="0a94b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a94b-116">-ResourceGroupName</span></span>
<span data-ttu-id="0a94b-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a94b-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="0a94b-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a94b-118">-WorkspaceName</span></span>
<span data-ttu-id="0a94b-119">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a94b-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="0a94b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a94b-120">CommonParameters</span></span>
<span data-ttu-id="0a94b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a94b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a94b-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a94b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a94b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a94b-123">INPUTS</span></span>

### <span data-ttu-id="0a94b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0a94b-124">System.String</span></span>

### <span data-ttu-id="0a94b-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a94b-125">System.Boolean</span></span>

## <span data-ttu-id="0a94b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a94b-126">OUTPUTS</span></span>

### <span data-ttu-id="0a94b-127">Microsoft. Azure. Command. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="0a94b-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="0a94b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a94b-128">NOTES</span></span>

## <span data-ttu-id="0a94b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a94b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a94b-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a94b-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


