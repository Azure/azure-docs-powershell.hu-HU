---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014810"
---
# <span data-ttu-id="2df76-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2df76-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="2df76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2df76-102">SYNOPSIS</span></span>
<span data-ttu-id="2df76-103">Házirend-beállítás létrehozása a tűzfal házirendjéhez</span><span class="sxs-lookup"><span data-stu-id="2df76-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="2df76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2df76-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2df76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2df76-105">DESCRIPTION</span></span>
<span data-ttu-id="2df76-106">A **New-AzApplicationGatewayFirewallPolicySetting** házirend-beállításokat hoz létre a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="2df76-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="2df76-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2df76-107">EXAMPLES</span></span>

### <span data-ttu-id="2df76-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2df76-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="2df76-109">A parancs olyan házirend-beállítást hoz létre, amelyben a $enabledState, az üzemmód $enabledMode, a RequestBodyCheck hamis, a $fileUploadLimitInMb és a MaxRequestBodySizeInKb $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="2df76-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="2df76-110">Az új policySettings a rendszer a $condition-ra menti.</span><span class="sxs-lookup"><span data-stu-id="2df76-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="2df76-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2df76-111">PARAMETERS</span></span>

### <span data-ttu-id="2df76-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df76-112">-DefaultProfile</span></span>
<span data-ttu-id="2df76-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2df76-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df76-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="2df76-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="2df76-115">A requestBodyCheck a tűzfal házirend-beállításai között.</span><span class="sxs-lookup"><span data-stu-id="2df76-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2df76-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="2df76-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="2df76-117">FileUpload maximális mérete MB-ban</span><span class="sxs-lookup"><span data-stu-id="2df76-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="2df76-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="2df76-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="2df76-119">MaxRequestBodySizeInKb a tűzfalszabályok házirend-beállításai között.</span><span class="sxs-lookup"><span data-stu-id="2df76-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2df76-120">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="2df76-120">-Mode</span></span>
<span data-ttu-id="2df76-121">Tűzfal üzemmód a tűzfalszabályok házirend-beállításai között</span><span class="sxs-lookup"><span data-stu-id="2df76-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2df76-122">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="2df76-122">-State</span></span>
<span data-ttu-id="2df76-123">State változó a tűzfalszabályok házirend-beállításai között</span><span class="sxs-lookup"><span data-stu-id="2df76-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2df76-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df76-124">CommonParameters</span></span>
<span data-ttu-id="2df76-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2df76-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df76-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2df76-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df76-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df76-127">INPUTS</span></span>

### <span data-ttu-id="2df76-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="2df76-128">None</span></span>

## <span data-ttu-id="2df76-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df76-129">OUTPUTS</span></span>

### <span data-ttu-id="2df76-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="2df76-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="2df76-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2df76-131">NOTES</span></span>

## <span data-ttu-id="2df76-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2df76-132">RELATED LINKS</span></span>
