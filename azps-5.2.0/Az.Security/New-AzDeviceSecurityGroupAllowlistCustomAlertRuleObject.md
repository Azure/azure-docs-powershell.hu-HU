---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337397"
---
# <span data-ttu-id="7c956-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="7c956-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="7c956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c956-102">SYNOPSIS</span></span>
<span data-ttu-id="7c956-103">Új egyéni értesítési szabály létrehozása az eszköz biztonsági csoportjához (IoT-biztonság)</span><span class="sxs-lookup"><span data-stu-id="7c956-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="7c956-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c956-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c956-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c956-105">DESCRIPTION</span></span>
<span data-ttu-id="7c956-106">A New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject parancsmag létrehoz egy új listát az eszköz biztonsági csoportjának engedélyezett egyéni riasztási szabályairól az IoT biztonsági megoldásban.</span><span class="sxs-lookup"><span data-stu-id="7c956-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="7c956-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c956-107">EXAMPLES</span></span>

### <span data-ttu-id="7c956-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c956-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="7c956-109">Új engedélyezett lista egyéni riasztási rull létrehozása a "LocalUserNotAllowed" típusból, letiltható állapottal</span><span class="sxs-lookup"><span data-stu-id="7c956-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="7c956-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c956-110">PARAMETERS</span></span>

### <span data-ttu-id="7c956-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="7c956-111">-AllowlistValue</span></span>
<span data-ttu-id="7c956-112">Listaértékek engedélyezése</span><span class="sxs-lookup"><span data-stu-id="7c956-112">Allow list values.</span></span>

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

### <span data-ttu-id="7c956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c956-113">-DefaultProfile</span></span>
<span data-ttu-id="7c956-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c956-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c956-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="7c956-115">-Enabled</span></span>
<span data-ttu-id="7c956-116">Engedélyezve van a szabály?</span><span class="sxs-lookup"><span data-stu-id="7c956-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="7c956-117">-Type</span><span class="sxs-lookup"><span data-stu-id="7c956-117">-Type</span></span>
<span data-ttu-id="7c956-118">Szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="7c956-118">Rule type.</span></span>

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

### <span data-ttu-id="7c956-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c956-119">CommonParameters</span></span>
<span data-ttu-id="7c956-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c956-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c956-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c956-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c956-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c956-122">INPUTS</span></span>

### <span data-ttu-id="7c956-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c956-123">None</span></span>

## <span data-ttu-id="7c956-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c956-124">OUTPUTS</span></span>

### <span data-ttu-id="7c956-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="7c956-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="7c956-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c956-126">NOTES</span></span>

## <span data-ttu-id="7c956-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c956-127">RELATED LINKS</span></span>
