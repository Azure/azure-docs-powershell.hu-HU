---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672204"
---
# <span data-ttu-id="d6229-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="d6229-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="d6229-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6229-102">SYNOPSIS</span></span>
<span data-ttu-id="d6229-103">Engedélyezi vagy letiltja a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="d6229-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6229-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6229-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6229-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6229-105">DESCRIPTION</span></span>
<span data-ttu-id="d6229-106">A **set-AzureRmOperationalInsightsIntelligencePack** parancsmag lehetővé teszi a megadott intelligencia-csomag beállítását, ha be van *kapcsolva* a $True, és letiltja azt, ha az *engedélyezve* beállítás értéke $false.</span><span class="sxs-lookup"><span data-stu-id="d6229-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="d6229-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6229-107">EXAMPLES</span></span>

### <span data-ttu-id="d6229-108">1. példa: a hírszerzési csomagok beállítása</span><span class="sxs-lookup"><span data-stu-id="d6229-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="d6229-109">Ez a parancs engedélyezi a megadott intelligencia csomagot.</span><span class="sxs-lookup"><span data-stu-id="d6229-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="d6229-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6229-110">PARAMETERS</span></span>

### <span data-ttu-id="d6229-111">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d6229-111">-Enabled</span></span>
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

### <span data-ttu-id="d6229-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="d6229-112">-IntelligencePackName</span></span>
<span data-ttu-id="d6229-113">A hírszerzési csomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6229-113">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="d6229-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6229-114">-ResourceGroupName</span></span>
<span data-ttu-id="d6229-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6229-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="d6229-116">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6229-116">-WorkspaceName</span></span>
<span data-ttu-id="d6229-117">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6229-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="d6229-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6229-118">-DefaultProfile</span></span>
<span data-ttu-id="d6229-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6229-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6229-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6229-120">CommonParameters</span></span>
<span data-ttu-id="d6229-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6229-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6229-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6229-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6229-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6229-123">INPUTS</span></span>

## <span data-ttu-id="d6229-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6229-124">OUTPUTS</span></span>

## <span data-ttu-id="d6229-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6229-125">NOTES</span></span>

## <span data-ttu-id="d6229-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6229-126">RELATED LINKS</span></span>

[<span data-ttu-id="d6229-127">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d6229-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


