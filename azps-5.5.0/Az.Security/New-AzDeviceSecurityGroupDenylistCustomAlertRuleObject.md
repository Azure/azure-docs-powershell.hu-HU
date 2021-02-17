---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208319"
---
# <span data-ttu-id="8e796-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="8e796-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="8e796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e796-102">SYNOPSIS</span></span>
<span data-ttu-id="8e796-103">Új elutasítási lista egyéni riasztási szabályának létrehozása az eszköz biztonsági csoportjához (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="8e796-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="8e796-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e796-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e796-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e796-105">DESCRIPTION</span></span>
<span data-ttu-id="8e796-106">A New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject parancsmag létrehoz egy új listát az eszköz biztonsági csoportjának elutasított egyéni riasztási szabályairól az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="8e796-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="8e796-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e796-107">EXAMPLES</span></span>

### <span data-ttu-id="8e796-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e796-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="8e796-109">Új elutasítási lista egyéni riasztási szabályának létrehozása a "SomeRuleType" típussal és az állapot desable (Desable) beállítással</span><span class="sxs-lookup"><span data-stu-id="8e796-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="8e796-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e796-110">PARAMETERS</span></span>

### <span data-ttu-id="8e796-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e796-111">-DefaultProfile</span></span>
<span data-ttu-id="8e796-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e796-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e796-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="8e796-113">-DenylistValue</span></span>
<span data-ttu-id="8e796-114">Listaértékek elutasítása</span><span class="sxs-lookup"><span data-stu-id="8e796-114">Deny list values.</span></span>

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

### <span data-ttu-id="8e796-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8e796-115">-Enabled</span></span>
<span data-ttu-id="8e796-116">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="8e796-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="8e796-117">-Type</span><span class="sxs-lookup"><span data-stu-id="8e796-117">-Type</span></span>
<span data-ttu-id="8e796-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="8e796-118">Rule type.</span></span>

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

### <span data-ttu-id="8e796-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e796-119">CommonParameters</span></span>
<span data-ttu-id="8e796-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e796-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e796-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e796-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e796-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e796-122">INPUTS</span></span>

### <span data-ttu-id="8e796-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e796-123">None</span></span>

## <span data-ttu-id="8e796-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e796-124">OUTPUTS</span></span>

### <span data-ttu-id="8e796-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="8e796-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="8e796-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e796-126">NOTES</span></span>

## <span data-ttu-id="8e796-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e796-127">RELATED LINKS</span></span>
