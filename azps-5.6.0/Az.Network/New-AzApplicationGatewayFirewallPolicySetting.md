---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923985"
---
# <span data-ttu-id="098a3-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="098a3-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="098a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098a3-102">SYNOPSIS</span></span>
<span data-ttu-id="098a3-103">Házirendbeállítás létrehozása a tűzfal házirendhez</span><span class="sxs-lookup"><span data-stu-id="098a3-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="098a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="098a3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="098a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="098a3-105">DESCRIPTION</span></span>
<span data-ttu-id="098a3-106">A **New-AzApplicationGatewayFirewallPolicySetting létrehoz** egy házirend-beállítást egy tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="098a3-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="098a3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="098a3-107">EXAMPLES</span></span>

### <span data-ttu-id="098a3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="098a3-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="098a3-109">A parancs létrehoz egy házirend-beállítást $enabledState állammal, $enabledMode móddal, a RequestCheck mint false, a FileUploadLimitInMb mint $fileUploadLimitInMb és a MaxRequestQuestSizeInKb értékeket $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="098a3-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="098a3-110">Az új házirendBeállítók tárolása a következő $condition.</span><span class="sxs-lookup"><span data-stu-id="098a3-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="098a3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="098a3-111">PARAMETERS</span></span>

### <span data-ttu-id="098a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098a3-112">-DefaultProfile</span></span>
<span data-ttu-id="098a3-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="098a3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="098a3-114">-DisableRequestCheck</span><span class="sxs-lookup"><span data-stu-id="098a3-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="098a3-115">Diables the requestCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="098a3-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098a3-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="098a3-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="098a3-117">Fájlfrissítés maximális mérete MB-ban.</span><span class="sxs-lookup"><span data-stu-id="098a3-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098a3-118">-MaxRequestQuestSizeInKb</span><span class="sxs-lookup"><span data-stu-id="098a3-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="098a3-119">MaxRequestQuestQuestSizeInKb a tűzfal házirend-beállításai között.</span><span class="sxs-lookup"><span data-stu-id="098a3-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098a3-120">-Mód</span><span class="sxs-lookup"><span data-stu-id="098a3-120">-Mode</span></span>
<span data-ttu-id="098a3-121">Tűzfal mód a tűzfal házirend-beállításai között.</span><span class="sxs-lookup"><span data-stu-id="098a3-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098a3-122">-State</span><span class="sxs-lookup"><span data-stu-id="098a3-122">-State</span></span>
<span data-ttu-id="098a3-123">State variable in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="098a3-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098a3-124">CommonParameters</span></span>
<span data-ttu-id="098a3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098a3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="098a3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098a3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="098a3-127">INPUTS</span></span>

### <span data-ttu-id="098a3-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="098a3-128">None</span></span>

## <span data-ttu-id="098a3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="098a3-129">OUTPUTS</span></span>

### <span data-ttu-id="098a3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="098a3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="098a3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="098a3-131">NOTES</span></span>

## <span data-ttu-id="098a3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="098a3-132">RELATED LINKS</span></span>
