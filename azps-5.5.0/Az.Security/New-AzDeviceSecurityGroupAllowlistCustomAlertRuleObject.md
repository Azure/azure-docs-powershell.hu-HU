---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165147"
---
# <span data-ttu-id="55e6b-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="55e6b-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="55e6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="55e6b-103">Új egyéni értesítési szabály létrehozása az eszköz biztonsági csoportjához (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="55e6b-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="55e6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55e6b-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e6b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="55e6b-106">A New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject parancsmag létrehoz egy új listát az eszköz biztonsági csoportjának engedélyezett egyéni riasztási szabályairól az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="55e6b-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="55e6b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="55e6b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="55e6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="55e6b-109">Új, "LocalUserNotAllowed" típusból származó, az engedélyezettek listáját engedélyező egyéni riasztási rull létrehozása letiltani beállított állapottal</span><span class="sxs-lookup"><span data-stu-id="55e6b-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="55e6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="55e6b-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="55e6b-111">-AllowlistValue</span></span>
<span data-ttu-id="55e6b-112">Listaértékek engedélyezése</span><span class="sxs-lookup"><span data-stu-id="55e6b-112">Allow list values.</span></span>

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

### <span data-ttu-id="55e6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e6b-113">-DefaultProfile</span></span>
<span data-ttu-id="55e6b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55e6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e6b-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="55e6b-115">-Enabled</span></span>
<span data-ttu-id="55e6b-116">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="55e6b-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="55e6b-117">-Type</span><span class="sxs-lookup"><span data-stu-id="55e6b-117">-Type</span></span>
<span data-ttu-id="55e6b-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="55e6b-118">Rule type.</span></span>

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

### <span data-ttu-id="55e6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e6b-119">CommonParameters</span></span>
<span data-ttu-id="55e6b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e6b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55e6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e6b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55e6b-122">INPUTS</span></span>

### <span data-ttu-id="55e6b-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="55e6b-123">None</span></span>

## <span data-ttu-id="55e6b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55e6b-124">OUTPUTS</span></span>

### <span data-ttu-id="55e6b-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="55e6b-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="55e6b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55e6b-126">NOTES</span></span>

## <span data-ttu-id="55e6b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55e6b-127">RELATED LINKS</span></span>
