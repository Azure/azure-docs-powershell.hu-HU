---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024454"
---
# <span data-ttu-id="e6b54-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="e6b54-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="e6b54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6b54-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b54-103">Új küszöbérték létrehozása egyéni figyelmeztetési szabály az eszközök biztonsági csoportjához (IoT biztonsága)</span><span class="sxs-lookup"><span data-stu-id="e6b54-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="e6b54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6b54-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6b54-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b54-106">A New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject parancsmag új listát hoz létre a küszöbértékekkel kapcsolatos egyéni figyelmeztetési szabályokról az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="e6b54-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="e6b54-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6b54-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b54-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6b54-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="e6b54-109">Új küszöbérték létrehozása egyéni figyelmeztetési szabály a "SomeRuleType" típustól a minimális és a maximális küszöbértékhez tartozó állapot engedélyezve Ant-értékekkel</span><span class="sxs-lookup"><span data-stu-id="e6b54-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="e6b54-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6b54-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b54-111">-DefaultProfile</span></span>
<span data-ttu-id="e6b54-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6b54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b54-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="e6b54-113">-Enabled</span></span>
<span data-ttu-id="e6b54-114">A szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e6b54-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b54-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="e6b54-115">-MaxThreshold</span></span>
<span data-ttu-id="e6b54-116">Maximális küszöb</span><span class="sxs-lookup"><span data-stu-id="e6b54-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="e6b54-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="e6b54-117">-MinThreshold</span></span>
<span data-ttu-id="e6b54-118">Minimális küszöb</span><span class="sxs-lookup"><span data-stu-id="e6b54-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="e6b54-119">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e6b54-119">-Type</span></span>
<span data-ttu-id="e6b54-120">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="e6b54-120">Rule type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b54-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b54-121">CommonParameters</span></span>
<span data-ttu-id="e6b54-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6b54-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b54-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6b54-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b54-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b54-124">INPUTS</span></span>

### <span data-ttu-id="e6b54-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6b54-125">None</span></span>

## <span data-ttu-id="e6b54-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b54-126">OUTPUTS</span></span>

### <span data-ttu-id="e6b54-127">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="e6b54-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="e6b54-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6b54-128">NOTES</span></span>

## <span data-ttu-id="e6b54-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6b54-129">RELATED LINKS</span></span>
