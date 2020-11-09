---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300836"
---
# <span data-ttu-id="bb766-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="bb766-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="bb766-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb766-102">SYNOPSIS</span></span>
<span data-ttu-id="bb766-103">Egy megbízható házirend-aláíró felvétele a bérlő számára az Azure tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="bb766-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bb766-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb766-104">SYNTAX</span></span>

### <span data-ttu-id="bb766-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb766-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb766-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb766-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb766-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb766-107">DESCRIPTION</span></span>
<span data-ttu-id="bb766-108">Az Add-AzAttestationPolicySigner parancsmag egy megbízható házirend-aláírót ad a bérlőnek az Azure tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="bb766-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bb766-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bb766-109">EXAMPLES</span></span>

### <span data-ttu-id="bb766-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb766-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="bb766-111">Adjon hozzá egy megbízható aláírót a *pshtest* nevű Atteestation-szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="bb766-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="bb766-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb766-112">PARAMETERS</span></span>

### <span data-ttu-id="bb766-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb766-113">-DefaultProfile</span></span>
<span data-ttu-id="bb766-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb766-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb766-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb766-115">-Name</span></span>
<span data-ttu-id="bb766-116">A tanúsítvány-szolgáltató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb766-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb766-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb766-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb766-118">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb766-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb766-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb766-119">-ResourceId</span></span>
<span data-ttu-id="bb766-120">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb766-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb766-121">– Aláíró</span><span class="sxs-lookup"><span data-stu-id="bb766-121">-Signer</span></span>
<span data-ttu-id="bb766-122">A "Maa-policyCertificate" jogcím nevű RFC7519 JSON-webtokent adja meg, amelynek az értéke egy RFC7517 JSON-webkulcs, amely egy új, megbízható aláírási kulcsot tartalmaz a hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="bb766-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="bb766-123">A RFC7519 JWT be kell jelentkeznie a meglévő megbízható aláírási kulcsok egyikével.</span><span class="sxs-lookup"><span data-stu-id="bb766-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="bb766-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb766-124">-Confirm</span></span>
<span data-ttu-id="bb766-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb766-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb766-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb766-126">-WhatIf</span></span>
<span data-ttu-id="bb766-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb766-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb766-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb766-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb766-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb766-129">CommonParameters</span></span>
<span data-ttu-id="bb766-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb766-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb766-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb766-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb766-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb766-132">INPUTS</span></span>

### <span data-ttu-id="bb766-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb766-133">System.String</span></span>

## <span data-ttu-id="bb766-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb766-134">OUTPUTS</span></span>

### <span data-ttu-id="bb766-135">Microsoft. Azure. commands. igazolás. models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="bb766-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="bb766-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb766-136">NOTES</span></span>

## <span data-ttu-id="bb766-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb766-137">RELATED LINKS</span></span>
