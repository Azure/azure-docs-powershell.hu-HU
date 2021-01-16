---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377759"
---
# <span data-ttu-id="8d907-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="8d907-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="8d907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d907-102">SYNOPSIS</span></span>
<span data-ttu-id="8d907-103">Új küszöbérték egyéni riasztási szabály létrehozása eszközbiztonsági csoporthoz (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="8d907-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="8d907-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d907-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d907-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d907-105">DESCRIPTION</span></span>
<span data-ttu-id="8d907-106">A New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject parancsmag létrehoz egy új listát a küszöbérték egyéni riasztási szabályairól az Eszközbiztonsági csoport számára az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="8d907-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="8d907-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d907-107">EXAMPLES</span></span>

### <span data-ttu-id="8d907-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d907-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="8d907-109">Új küszöbérték egyéni riasztási szabály létrehozása a "SomeRuleType" típusból az állapot engedélyezett ant értékekkel a minimális és a maximális küszöbértékhez</span><span class="sxs-lookup"><span data-stu-id="8d907-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="8d907-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d907-110">PARAMETERS</span></span>

### <span data-ttu-id="8d907-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d907-111">-DefaultProfile</span></span>
<span data-ttu-id="8d907-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d907-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d907-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8d907-113">-Enabled</span></span>
<span data-ttu-id="8d907-114">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="8d907-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="8d907-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="8d907-115">-MaxThreshold</span></span>
<span data-ttu-id="8d907-116">Maximális küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="8d907-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="8d907-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="8d907-117">-MinThreshold</span></span>
<span data-ttu-id="8d907-118">Minimális küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="8d907-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="8d907-119">-Type</span><span class="sxs-lookup"><span data-stu-id="8d907-119">-Type</span></span>
<span data-ttu-id="8d907-120">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="8d907-120">Rule type.</span></span>

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

### <span data-ttu-id="8d907-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d907-121">CommonParameters</span></span>
<span data-ttu-id="8d907-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d907-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d907-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d907-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d907-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d907-124">INPUTS</span></span>

### <span data-ttu-id="8d907-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d907-125">None</span></span>

## <span data-ttu-id="8d907-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d907-126">OUTPUTS</span></span>

### <span data-ttu-id="8d907-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="8d907-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="8d907-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d907-128">NOTES</span></span>

## <span data-ttu-id="8d907-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d907-129">RELATED LINKS</span></span>
