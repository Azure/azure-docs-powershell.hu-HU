---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011878"
---
# <span data-ttu-id="448f8-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="448f8-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="448f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448f8-102">SYNOPSIS</span></span>
<span data-ttu-id="448f8-103">Új Azure firewall policy intrusion Detection Signature Override</span><span class="sxs-lookup"><span data-stu-id="448f8-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="448f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="448f8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448f8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="448f8-105">DESCRIPTION</span></span>
<span data-ttu-id="448f8-106">A **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** parancsmag létrehoz egy Azure Tűzfalházi házirend aláírás-felülbírálási objektumát.</span><span class="sxs-lookup"><span data-stu-id="448f8-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="448f8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="448f8-107">EXAMPLES</span></span>

### <span data-ttu-id="448f8-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="448f8-108">Example 1: 1.</span></span> <span data-ttu-id="448f8-109">Beszúrás észlelése aláírás-felülbírálásokkal</span><span class="sxs-lookup"><span data-stu-id="448f8-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="448f8-110">Ebben a példában a beszúrás észlelése adott aláírás-felülbírálással elutasítási módban</span><span class="sxs-lookup"><span data-stu-id="448f8-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="448f8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="448f8-111">PARAMETERS</span></span>

### <span data-ttu-id="448f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448f8-112">-DefaultProfile</span></span>
<span data-ttu-id="448f8-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="448f8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f8-114">-Id</span><span class="sxs-lookup"><span data-stu-id="448f8-114">-Id</span></span>
<span data-ttu-id="448f8-115">Aláírásazonosító.</span><span class="sxs-lookup"><span data-stu-id="448f8-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f8-116">-Mód</span><span class="sxs-lookup"><span data-stu-id="448f8-116">-Mode</span></span>
<span data-ttu-id="448f8-117">Aláírás állapota.</span><span class="sxs-lookup"><span data-stu-id="448f8-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="448f8-118">-Confirm</span></span>
<span data-ttu-id="448f8-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="448f8-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448f8-120">-WhatIf</span></span>
<span data-ttu-id="448f8-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="448f8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448f8-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="448f8-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448f8-123">CommonParameters</span></span>
<span data-ttu-id="448f8-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448f8-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="448f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448f8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="448f8-126">INPUTS</span></span>

### <span data-ttu-id="448f8-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="448f8-127">None</span></span>

## <span data-ttu-id="448f8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="448f8-128">OUTPUTS</span></span>

### <span data-ttu-id="448f8-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="448f8-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="448f8-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="448f8-130">NOTES</span></span>

## <span data-ttu-id="448f8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="448f8-131">RELATED LINKS</span></span>
