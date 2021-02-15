---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151699"
---
# <span data-ttu-id="123b4-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="123b4-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="123b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123b4-102">SYNOPSIS</span></span>
<span data-ttu-id="123b4-103">Új Azure firewall policy intrusion Detection Signature Override</span><span class="sxs-lookup"><span data-stu-id="123b4-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="123b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="123b4-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="123b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="123b4-105">DESCRIPTION</span></span>
<span data-ttu-id="123b4-106">A **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** parancsmag létrehoz egy Azure Tűzfalházi házirend aláírás-felülbírálási objektumát.</span><span class="sxs-lookup"><span data-stu-id="123b4-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="123b4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="123b4-107">EXAMPLES</span></span>

### <span data-ttu-id="123b4-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="123b4-108">Example 1: 1.</span></span> <span data-ttu-id="123b4-109">Beszúrás észlelése aláírás-felülbírálásokkal</span><span class="sxs-lookup"><span data-stu-id="123b4-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="123b4-110">Ez a példa beszúrási észlelést hoz létre az elutasítási módra adott aláírás-felülbírálással</span><span class="sxs-lookup"><span data-stu-id="123b4-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="123b4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="123b4-111">PARAMETERS</span></span>

### <span data-ttu-id="123b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123b4-112">-DefaultProfile</span></span>
<span data-ttu-id="123b4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="123b4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="123b4-114">-Id</span><span class="sxs-lookup"><span data-stu-id="123b4-114">-Id</span></span>
<span data-ttu-id="123b4-115">Aláírásazonosító.</span><span class="sxs-lookup"><span data-stu-id="123b4-115">Signature id.</span></span>

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

### <span data-ttu-id="123b4-116">-Mód</span><span class="sxs-lookup"><span data-stu-id="123b4-116">-Mode</span></span>
<span data-ttu-id="123b4-117">Aláírás állapota.</span><span class="sxs-lookup"><span data-stu-id="123b4-117">Signature state.</span></span>

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

### <span data-ttu-id="123b4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="123b4-118">-Confirm</span></span>
<span data-ttu-id="123b4-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="123b4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="123b4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="123b4-120">-WhatIf</span></span>
<span data-ttu-id="123b4-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="123b4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="123b4-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="123b4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="123b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123b4-123">CommonParameters</span></span>
<span data-ttu-id="123b4-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123b4-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="123b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123b4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="123b4-126">INPUTS</span></span>

### <span data-ttu-id="123b4-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="123b4-127">None</span></span>

## <span data-ttu-id="123b4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="123b4-128">OUTPUTS</span></span>

### <span data-ttu-id="123b4-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="123b4-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="123b4-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="123b4-130">NOTES</span></span>

## <span data-ttu-id="123b4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="123b4-131">RELATED LINKS</span></span>
