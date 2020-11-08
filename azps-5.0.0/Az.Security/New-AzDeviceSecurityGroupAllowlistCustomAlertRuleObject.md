---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195657"
---
# <span data-ttu-id="4dbed-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="4dbed-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="4dbed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dbed-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbed-103">Új engedélyezési lista létrehozása egyéni figyelmeztetési szabály az eszközök biztonsági csoportjához (IoT biztonsága)</span><span class="sxs-lookup"><span data-stu-id="4dbed-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="4dbed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dbed-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dbed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dbed-105">DESCRIPTION</span></span>
<span data-ttu-id="4dbed-106">A New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject parancsmag új listát hoz létre az engedélyezett egyéni figyelmeztetési szabályokról a IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="4dbed-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="4dbed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4dbed-107">EXAMPLES</span></span>

### <span data-ttu-id="4dbed-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4dbed-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="4dbed-109">Új engedélyezési lista létrehozása egyéni riasztási Rull a "LocalUserNotAllowed" típust letiltva</span><span class="sxs-lookup"><span data-stu-id="4dbed-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="4dbed-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dbed-110">PARAMETERS</span></span>

### <span data-ttu-id="4dbed-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="4dbed-111">-AllowlistValue</span></span>
<span data-ttu-id="4dbed-112">Listaelemek engedélyezése</span><span class="sxs-lookup"><span data-stu-id="4dbed-112">Allow list values.</span></span>

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

### <span data-ttu-id="4dbed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbed-113">-DefaultProfile</span></span>
<span data-ttu-id="4dbed-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dbed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dbed-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4dbed-115">-Enabled</span></span>
<span data-ttu-id="4dbed-116">A szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4dbed-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="4dbed-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="4dbed-117">-Type</span></span>
<span data-ttu-id="4dbed-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="4dbed-118">Rule type.</span></span>

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

### <span data-ttu-id="4dbed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbed-119">CommonParameters</span></span>
<span data-ttu-id="4dbed-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dbed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbed-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4dbed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbed-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dbed-122">INPUTS</span></span>

### <span data-ttu-id="4dbed-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="4dbed-123">None</span></span>

## <span data-ttu-id="4dbed-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dbed-124">OUTPUTS</span></span>

### <span data-ttu-id="4dbed-125">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="4dbed-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="4dbed-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dbed-126">NOTES</span></span>

## <span data-ttu-id="4dbed-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dbed-127">RELATED LINKS</span></span>
