---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932250"
---
# <span data-ttu-id="d21b7-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d21b7-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="d21b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d21b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d21b7-103">Új elutasítási lista egyéni riasztási szabályának létrehozása az eszköz biztonsági csoportjához (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="d21b7-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d21b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d21b7-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d21b7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d21b7-105">DESCRIPTION</span></span>
<span data-ttu-id="d21b7-106">A New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject parancsmag létrehoz egy új listát, amely felsorolja az eszközbiztonsági csoportokra vonatkozó egyéni riasztási szabályokat az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="d21b7-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d21b7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d21b7-107">EXAMPLES</span></span>

### <span data-ttu-id="d21b7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d21b7-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="d21b7-109">Új elutasítási lista egyéni riasztási szabályának létrehozása a "SomeRuleType" típussal és az állapot desable (Desable) beállítással</span><span class="sxs-lookup"><span data-stu-id="d21b7-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="d21b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d21b7-110">PARAMETERS</span></span>

### <span data-ttu-id="d21b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21b7-111">-DefaultProfile</span></span>
<span data-ttu-id="d21b7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d21b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d21b7-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="d21b7-113">-DenylistValue</span></span>
<span data-ttu-id="d21b7-114">Listaértékek elutasítása</span><span class="sxs-lookup"><span data-stu-id="d21b7-114">Deny list values.</span></span>

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

### <span data-ttu-id="d21b7-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d21b7-115">-Enabled</span></span>
<span data-ttu-id="d21b7-116">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="d21b7-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="d21b7-117">-Type</span><span class="sxs-lookup"><span data-stu-id="d21b7-117">-Type</span></span>
<span data-ttu-id="d21b7-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="d21b7-118">Rule type.</span></span>

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

### <span data-ttu-id="d21b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21b7-119">CommonParameters</span></span>
<span data-ttu-id="d21b7-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d21b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21b7-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d21b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21b7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d21b7-122">INPUTS</span></span>

### <span data-ttu-id="d21b7-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d21b7-123">None</span></span>

## <span data-ttu-id="d21b7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d21b7-124">OUTPUTS</span></span>

### <span data-ttu-id="d21b7-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d21b7-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="d21b7-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d21b7-126">NOTES</span></span>

## <span data-ttu-id="d21b7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d21b7-127">RELATED LINKS</span></span>
