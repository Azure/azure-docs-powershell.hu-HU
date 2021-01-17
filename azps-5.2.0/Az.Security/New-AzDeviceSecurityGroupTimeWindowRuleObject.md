---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337325"
---
# <span data-ttu-id="35743-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="35743-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="35743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35743-102">SYNOPSIS</span></span>
<span data-ttu-id="35743-103">Új időkeretszabály létrehozása eszközbiztonsági csoporthoz (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="35743-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="35743-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35743-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35743-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35743-105">DESCRIPTION</span></span>
<span data-ttu-id="35743-106">A New-AzDeviceSecurityGroupTimeWindowRuleObject parancsmag létrehoz egy új időablak-riasztási szabályokat az eszköz biztonsági csoportjához az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="35743-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="35743-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35743-107">EXAMPLES</span></span>

### <span data-ttu-id="35743-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="35743-108">Example 1</span></span>
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

<span data-ttu-id="35743-109">Új időkeretszabály létrehozása az "ActiveConnectionsNotInAllowedRange" típusból</span><span class="sxs-lookup"><span data-stu-id="35743-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="35743-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35743-110">PARAMETERS</span></span>

### <span data-ttu-id="35743-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35743-111">-DefaultProfile</span></span>
<span data-ttu-id="35743-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35743-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35743-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="35743-113">-Enabled</span></span>
<span data-ttu-id="35743-114">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="35743-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="35743-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="35743-115">-MaxThreshold</span></span>
<span data-ttu-id="35743-116">Maximális küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="35743-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="35743-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="35743-117">-MinThreshold</span></span>
<span data-ttu-id="35743-118">Minimális küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="35743-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="35743-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="35743-119">-TimeWindowSize</span></span>
<span data-ttu-id="35743-120">Időablak mérete.</span><span class="sxs-lookup"><span data-stu-id="35743-120">Time window size.</span></span>

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

### <span data-ttu-id="35743-121">-Type</span><span class="sxs-lookup"><span data-stu-id="35743-121">-Type</span></span>
<span data-ttu-id="35743-122">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="35743-122">Rule type.</span></span>

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

### <span data-ttu-id="35743-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35743-123">CommonParameters</span></span>
<span data-ttu-id="35743-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35743-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35743-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35743-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35743-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35743-126">INPUTS</span></span>

### <span data-ttu-id="35743-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="35743-127">None</span></span>

## <span data-ttu-id="35743-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35743-128">OUTPUTS</span></span>

### <span data-ttu-id="35743-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="35743-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="35743-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35743-130">NOTES</span></span>

## <span data-ttu-id="35743-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35743-131">RELATED LINKS</span></span>
