---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183989"
---
# <span data-ttu-id="866d3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="866d3-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="866d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="866d3-102">SYNOPSIS</span></span>
<span data-ttu-id="866d3-103">Új időablak-szabály létrehozása az eszközök biztonsági csoportjához (IoT biztonsága)</span><span class="sxs-lookup"><span data-stu-id="866d3-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="866d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="866d3-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="866d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="866d3-105">DESCRIPTION</span></span>
<span data-ttu-id="866d3-106">Az New-AzDeviceSecurityGroupTimeWindowRuleObject parancsmag az IoT biztonsági megoldásban az eszközök biztonsági csoportjának új időablakos figyelmeztetési szabályainak új listáját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="866d3-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="866d3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="866d3-107">EXAMPLES</span></span>

### <span data-ttu-id="866d3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="866d3-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="866d3-109">Új időablak-szabály létrehozása "ActiveConnectionsNotInAllowedRange" típusból</span><span class="sxs-lookup"><span data-stu-id="866d3-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="866d3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="866d3-110">PARAMETERS</span></span>

### <span data-ttu-id="866d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866d3-111">-DefaultProfile</span></span>
<span data-ttu-id="866d3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="866d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866d3-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="866d3-113">-Enabled</span></span>
<span data-ttu-id="866d3-114">A szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="866d3-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="866d3-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="866d3-115">-MaxThreshold</span></span>
<span data-ttu-id="866d3-116">Maximális küszöb</span><span class="sxs-lookup"><span data-stu-id="866d3-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="866d3-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="866d3-117">-MinThreshold</span></span>
<span data-ttu-id="866d3-118">Minimális küszöb</span><span class="sxs-lookup"><span data-stu-id="866d3-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="866d3-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="866d3-119">-TimeWindowSize</span></span>
<span data-ttu-id="866d3-120">Az idő ablak mérete.</span><span class="sxs-lookup"><span data-stu-id="866d3-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866d3-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="866d3-121">-Type</span></span>
<span data-ttu-id="866d3-122">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="866d3-122">Rule type.</span></span>

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

### <span data-ttu-id="866d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866d3-123">CommonParameters</span></span>
<span data-ttu-id="866d3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="866d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866d3-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="866d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866d3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="866d3-126">INPUTS</span></span>

### <span data-ttu-id="866d3-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="866d3-127">None</span></span>

## <span data-ttu-id="866d3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="866d3-128">OUTPUTS</span></span>

### <span data-ttu-id="866d3-129">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="866d3-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="866d3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="866d3-130">NOTES</span></span>

## <span data-ttu-id="866d3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="866d3-131">RELATED LINKS</span></span>
