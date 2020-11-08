---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186734"
---
# <span data-ttu-id="4b6b7-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="4b6b7-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="4b6b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6b7-103">Új deny List listára vonatkozó egyéni figyelmeztetési szabály létrehozása az eszközök biztonsági csoportjához (IoT biztonsága)</span><span class="sxs-lookup"><span data-stu-id="4b6b7-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="4b6b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b6b7-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b6b7-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6b7-106">A New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject parancsmag új listát hoz létre a megtagadott egyéni figyelmeztetési szabályokról az IoT biztonsági megoldásban az eszközök biztonsági csoportjához.</span><span class="sxs-lookup"><span data-stu-id="4b6b7-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="4b6b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b6b7-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6b7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4b6b7-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="4b6b7-109">Új tiltó lista létrehozása egyéni figyelmeztetési szabály a Rull típus "SomeRuleType" és a status set to desuha</span><span class="sxs-lookup"><span data-stu-id="4b6b7-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="4b6b7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b6b7-110">PARAMETERS</span></span>

### <span data-ttu-id="4b6b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6b7-111">-DefaultProfile</span></span>
<span data-ttu-id="4b6b7-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b6b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b6b7-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="4b6b7-113">-DenylistValue</span></span>
<span data-ttu-id="4b6b7-114">Lista értékeinek elutasítása</span><span class="sxs-lookup"><span data-stu-id="4b6b7-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6b7-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4b6b7-115">-Enabled</span></span>
<span data-ttu-id="4b6b7-116">A szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4b6b7-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="4b6b7-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="4b6b7-117">-Type</span></span>
<span data-ttu-id="4b6b7-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="4b6b7-118">Rule type.</span></span>

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

### <span data-ttu-id="4b6b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6b7-119">CommonParameters</span></span>
<span data-ttu-id="4b6b7-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b6b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6b7-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4b6b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6b7-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6b7-122">INPUTS</span></span>

### <span data-ttu-id="4b6b7-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="4b6b7-123">None</span></span>

## <span data-ttu-id="4b6b7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6b7-124">OUTPUTS</span></span>

### <span data-ttu-id="4b6b7-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="4b6b7-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="4b6b7-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b6b7-126">NOTES</span></span>

## <span data-ttu-id="4b6b7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b6b7-127">RELATED LINKS</span></span>