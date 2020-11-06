---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491921"
---
# <span data-ttu-id="30ad7-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="30ad7-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="30ad7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="30ad7-103">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="30ad7-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30ad7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30ad7-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ad7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="30ad7-106">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="30ad7-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="30ad7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="30ad7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="30ad7-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="30ad7-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="30ad7-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="30ad7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30ad7-110">PARAMETERS</span></span>

### <span data-ttu-id="30ad7-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="30ad7-111">-Action</span></span>
<span data-ttu-id="30ad7-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="30ad7-112">Type of Actions.</span></span>
<span data-ttu-id="30ad7-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="30ad7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ad7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ad7-114">-DefaultProfile</span></span>
<span data-ttu-id="30ad7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30ad7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ad7-116">-Felülbírálja</span><span class="sxs-lookup"><span data-stu-id="30ad7-116">-Override</span></span>
<span data-ttu-id="30ad7-117">A overrideruleGroup ismertetése.</span><span class="sxs-lookup"><span data-stu-id="30ad7-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="30ad7-118">A lehetséges értékek a következők: "SqlInjection", "XSS"</span><span class="sxs-lookup"><span data-stu-id="30ad7-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ad7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ad7-119">CommonParameters</span></span>
<span data-ttu-id="30ad7-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30ad7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ad7-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ad7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ad7-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ad7-122">INPUTS</span></span>

### <span data-ttu-id="30ad7-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="30ad7-123">None</span></span>

## <span data-ttu-id="30ad7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ad7-124">OUTPUTS</span></span>

### <span data-ttu-id="30ad7-125">Microsoft. Azure. Command. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="30ad7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="30ad7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30ad7-126">NOTES</span></span>

## <span data-ttu-id="30ad7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30ad7-127">RELATED LINKS</span></span>

[<span data-ttu-id="30ad7-128">Új – AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="30ad7-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
