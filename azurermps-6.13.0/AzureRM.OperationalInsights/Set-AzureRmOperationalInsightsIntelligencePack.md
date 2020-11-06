---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494002"
---
# <span data-ttu-id="62557-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="62557-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="62557-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62557-102">SYNOPSIS</span></span>
<span data-ttu-id="62557-103">Engedélyezi vagy letiltja a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="62557-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62557-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62557-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62557-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62557-105">DESCRIPTION</span></span>
<span data-ttu-id="62557-106">A **set-AzureRmOperationalInsightsIntelligencePack** parancsmag lehetővé teszi a megadott intelligencia-csomag beállítását, ha be van *kapcsolva* a $True, és letiltja azt, ha az *engedélyezve* beállítás értéke $false.</span><span class="sxs-lookup"><span data-stu-id="62557-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="62557-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62557-107">EXAMPLES</span></span>

### <span data-ttu-id="62557-108">1. példa: a hírszerzési csomagok beállítása</span><span class="sxs-lookup"><span data-stu-id="62557-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="62557-109">Ez a parancs engedélyezi a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="62557-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="62557-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62557-110">PARAMETERS</span></span>

### <span data-ttu-id="62557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62557-111">-DefaultProfile</span></span>
<span data-ttu-id="62557-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62557-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62557-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="62557-113">-Enabled</span></span>
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

### <span data-ttu-id="62557-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="62557-114">-IntelligencePackName</span></span>
<span data-ttu-id="62557-115">A hírszerzési csomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62557-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="62557-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62557-116">-ResourceGroupName</span></span>
<span data-ttu-id="62557-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62557-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="62557-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62557-118">-WorkspaceName</span></span>
<span data-ttu-id="62557-119">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62557-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="62557-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62557-120">CommonParameters</span></span>
<span data-ttu-id="62557-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62557-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62557-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62557-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62557-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62557-123">INPUTS</span></span>

### <span data-ttu-id="62557-124">System. String</span><span class="sxs-lookup"><span data-stu-id="62557-124">System.String</span></span>

### <span data-ttu-id="62557-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62557-125">System.Boolean</span></span>

## <span data-ttu-id="62557-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62557-126">OUTPUTS</span></span>

### <span data-ttu-id="62557-127">Microsoft. Azure. Command. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="62557-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="62557-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62557-128">NOTES</span></span>

## <span data-ttu-id="62557-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62557-129">RELATED LINKS</span></span>

[<span data-ttu-id="62557-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="62557-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


