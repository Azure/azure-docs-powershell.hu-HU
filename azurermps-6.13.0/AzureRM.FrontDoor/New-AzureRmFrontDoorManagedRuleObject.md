---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672930"
---
# <span data-ttu-id="4daaa-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4daaa-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="4daaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4daaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4daaa-103">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4daaa-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4daaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4daaa-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4daaa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4daaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4daaa-106">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4daaa-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4daaa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4daaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4daaa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4daaa-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="4daaa-109">ManagedRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="4daaa-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="4daaa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4daaa-110">PARAMETERS</span></span>

### <span data-ttu-id="4daaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4daaa-111">-DefaultProfile</span></span>
<span data-ttu-id="4daaa-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4daaa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4daaa-113">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="4daaa-113">-Priority</span></span>
<span data-ttu-id="4daaa-114">A szabály prioritását ismerteti</span><span class="sxs-lookup"><span data-stu-id="4daaa-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4daaa-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4daaa-115">-RuleGroupOverride</span></span>
<span data-ttu-id="4daaa-116">Az Azure felügyelt szolgáltatóinak listája felülbírálja a konfigurációt</span><span class="sxs-lookup"><span data-stu-id="4daaa-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4daaa-117">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4daaa-117">-Version</span></span>
<span data-ttu-id="4daaa-118">A szabály verziószáma</span><span class="sxs-lookup"><span data-stu-id="4daaa-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4daaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4daaa-119">CommonParameters</span></span>
<span data-ttu-id="4daaa-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4daaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4daaa-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4daaa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4daaa-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4daaa-122">INPUTS</span></span>

### <span data-ttu-id="4daaa-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="4daaa-123">None</span></span>

## <span data-ttu-id="4daaa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4daaa-124">OUTPUTS</span></span>

### <span data-ttu-id="4daaa-125">Microsoft. Azure. Command. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="4daaa-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="4daaa-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4daaa-126">NOTES</span></span>

## <span data-ttu-id="4daaa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4daaa-127">RELATED LINKS</span></span>

<span data-ttu-id="4daaa-128">[Új – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Új – AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="4daaa-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
